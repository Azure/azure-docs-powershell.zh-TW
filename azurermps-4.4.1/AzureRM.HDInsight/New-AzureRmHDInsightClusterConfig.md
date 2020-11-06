---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456632"
---
# <span data-ttu-id="5c7f3-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5c7f3-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="5c7f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7f3-103">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c7f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c7f3-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c7f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="5c7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="5c7f3-106">**新的-AzureRmHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="5c7f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="5c7f3-107">EXAMPLES</span></span>

### <span data-ttu-id="5c7f3-108">範例1：建立群集設定物件</span><span class="sxs-lookup"><span data-stu-id="5c7f3-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="5c7f3-109">這個命令會建立群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="5c7f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c7f3-110">PARAMETERS</span></span>

### <span data-ttu-id="5c7f3-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="5c7f3-111">-AadTenantId</span></span>
<span data-ttu-id="5c7f3-112">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5c7f3-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="5c7f3-113">-CertificateFileContents</span></span>
<span data-ttu-id="5c7f3-114">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5c7f3-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="5c7f3-115">-CertificateFilePath</span></span>
<span data-ttu-id="5c7f3-116">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="5c7f3-117">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5c7f3-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5c7f3-118">-CertificatePassword</span></span>
<span data-ttu-id="5c7f3-119">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="5c7f3-120">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5c7f3-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="5c7f3-121">-ClusterTier</span></span>
<span data-ttu-id="5c7f3-122">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="5c7f3-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5c7f3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c7f3-124">標準</span><span class="sxs-lookup"><span data-stu-id="5c7f3-124">Standard</span></span>
- <span data-ttu-id="5c7f3-125">佳</span><span class="sxs-lookup"><span data-stu-id="5c7f3-125">Premium</span></span>

<span data-ttu-id="5c7f3-126">預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-126">The default value is Standard.</span></span>
<span data-ttu-id="5c7f3-127">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="5c7f3-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="5c7f3-128">-ClusterType</span></span>
<span data-ttu-id="5c7f3-129">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="5c7f3-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5c7f3-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c7f3-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="5c7f3-131">Hadoop</span></span>
- <span data-ttu-id="5c7f3-132">HBase</span><span class="sxs-lookup"><span data-stu-id="5c7f3-132">HBase</span></span>
- <span data-ttu-id="5c7f3-133">暴</span><span class="sxs-lookup"><span data-stu-id="5c7f3-133">Storm</span></span>
- <span data-ttu-id="5c7f3-134">Spark</span><span class="sxs-lookup"><span data-stu-id="5c7f3-134">Spark</span></span>

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

### <span data-ttu-id="5c7f3-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5c7f3-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="5c7f3-136">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="5c7f3-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5c7f3-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="5c7f3-138">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="5c7f3-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5c7f3-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="5c7f3-140">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="5c7f3-141">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="5c7f3-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="5c7f3-142">-EdgeNodeSize</span></span>
<span data-ttu-id="5c7f3-143">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="5c7f3-144">使用 Get-AzureRmVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="5c7f3-145">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="5c7f3-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="5c7f3-146">-HeadNodeSize</span></span>
<span data-ttu-id="5c7f3-147">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="5c7f3-148">使用 Get-AzureRMVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="5c7f3-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="5c7f3-149">-HiveMetastore</span></span>
<span data-ttu-id="5c7f3-150">指定要儲存 Hive 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="5c7f3-151">您也可以使用 Add-AzureRmHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="5c7f3-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5c7f3-152">-ObjectId</span></span>
<span data-ttu-id="5c7f3-153">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="5c7f3-154">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5c7f3-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="5c7f3-155">-OozieMetastore</span></span>
<span data-ttu-id="5c7f3-156">指定要儲存 Oozie 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="5c7f3-157">您也可以使用 **AzureRmHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="5c7f3-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="5c7f3-158">-WorkerNodeSize</span></span>
<span data-ttu-id="5c7f3-159">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="5c7f3-160">使用 Get-AzureRMVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="5c7f3-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="5c7f3-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="5c7f3-162">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="5c7f3-163">使用 Get-AzureRMVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="5c7f3-164">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="5c7f3-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7f3-165">-DefaultProfile</span></span>
<span data-ttu-id="5c7f3-166">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7f3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7f3-167">CommonParameters</span></span>
<span data-ttu-id="5c7f3-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7f3-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7f3-170">輸入</span><span class="sxs-lookup"><span data-stu-id="5c7f3-170">INPUTS</span></span>

## <span data-ttu-id="5c7f3-171">輸出</span><span class="sxs-lookup"><span data-stu-id="5c7f3-171">OUTPUTS</span></span>

### <span data-ttu-id="5c7f3-172">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="5c7f3-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5c7f3-173">筆記</span><span class="sxs-lookup"><span data-stu-id="5c7f3-173">NOTES</span></span>

## <span data-ttu-id="5c7f3-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c7f3-174">RELATED LINKS</span></span>

[<span data-ttu-id="5c7f3-175">附加 AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="5c7f3-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


