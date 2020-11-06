---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612291"
---
# New-AzHDInsightClusterConfig

## 摘要
建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。

## 句法

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**新的-AzHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。

## 示例

### 範例1：建立群集設定物件
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

這個命令會建立群集設定物件。

## 參數

### -AadTenantId
指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFileContents
指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFilePath
指定將用來以服務主體進行驗證的憑證檔案路徑。
當您存取 Azure Data Lake Store 時，群集會使用此程式。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
指定將用來驗證為服務主體之憑證的密碼。
當您存取 Azure Data Lake Store 時，群集會使用此程式。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterTier
指定 HDInsight 群集層級。
此參數可接受的值為：
- 標準
- [特優] 預設值為 [標準]。
[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
指定要建立的群集類型。
此參數可接受的值為：
- Hadoop
- HBase
- 暴
- Spark

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountType
指定 HDInsight 群集將使用的預設儲存空間類型。 可能的值為 AzureStorage 和 AzureDataLakeStore。

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### -EdgeNodeSize
指定邊緣節點的虛擬機器大小。 使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。 這個參數只對 RServer 群集有效。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeadNodeSize
指定頭節點的虛擬機器大小。
使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HiveMetastore
指定要儲存 Hive 中繼資料的 metastore。
您也可以使用 Add-AzHDInsightMetastore Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。
當您存取 Azure Data Lake Store 時，群集會使用此程式。

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OozieMetastore
指定要儲存 Oozie 中繼資料的 metastore。
您也可以使用 **AzHDInsightMetastore** Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkerNodeSize
指定工作人員節點的虛擬機器大小。
使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZookeeperNodeSize
指定 Zookeeper 節點的虛擬機器大小。
使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。
這個參數只對 HBase 或風暴群集有效。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### AzureHDInsightConfig （即 Azure。

## 筆記

## 相關連結

[附加 AzHDInsightStorage](./Add-AzHDInsightStorage.md)


