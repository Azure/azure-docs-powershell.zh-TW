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
ms.locfileid: "93787669"
---
# <span data-ttu-id="97d5f-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="97d5f-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="97d5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="97d5f-103">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="97d5f-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="97d5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="97d5f-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97d5f-105">說明</span><span class="sxs-lookup"><span data-stu-id="97d5f-105">DESCRIPTION</span></span>
<span data-ttu-id="97d5f-106">**新的-AzHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。</span><span class="sxs-lookup"><span data-stu-id="97d5f-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="97d5f-107">示例</span><span class="sxs-lookup"><span data-stu-id="97d5f-107">EXAMPLES</span></span>

### <span data-ttu-id="97d5f-108">範例1：建立群集設定物件</span><span class="sxs-lookup"><span data-stu-id="97d5f-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="97d5f-109">這個命令會建立群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="97d5f-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="97d5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="97d5f-110">PARAMETERS</span></span>

### <span data-ttu-id="97d5f-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="97d5f-111">-AadTenantId</span></span>
<span data-ttu-id="97d5f-112">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="97d5f-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="97d5f-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="97d5f-113">-CertificateFileContents</span></span>
<span data-ttu-id="97d5f-114">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="97d5f-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="97d5f-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="97d5f-115">-CertificateFilePath</span></span>
<span data-ttu-id="97d5f-116">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="97d5f-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="97d5f-117">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="97d5f-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="97d5f-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="97d5f-118">-CertificatePassword</span></span>
<span data-ttu-id="97d5f-119">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="97d5f-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="97d5f-120">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="97d5f-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="97d5f-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="97d5f-121">-ClusterTier</span></span>
<span data-ttu-id="97d5f-122">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="97d5f-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="97d5f-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="97d5f-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97d5f-124">標準</span><span class="sxs-lookup"><span data-stu-id="97d5f-124">Standard</span></span>
- <span data-ttu-id="97d5f-125">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="97d5f-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="97d5f-126">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="97d5f-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="97d5f-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="97d5f-127">-ClusterType</span></span>
<span data-ttu-id="97d5f-128">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="97d5f-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="97d5f-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="97d5f-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97d5f-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="97d5f-130">Hadoop</span></span>
- <span data-ttu-id="97d5f-131">HBase</span><span class="sxs-lookup"><span data-stu-id="97d5f-131">HBase</span></span>
- <span data-ttu-id="97d5f-132">暴</span><span class="sxs-lookup"><span data-stu-id="97d5f-132">Storm</span></span>
- <span data-ttu-id="97d5f-133">Spark</span><span class="sxs-lookup"><span data-stu-id="97d5f-133">Spark</span></span>

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

### <span data-ttu-id="97d5f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d5f-134">-DefaultProfile</span></span>
<span data-ttu-id="97d5f-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="97d5f-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97d5f-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="97d5f-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="97d5f-137">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="97d5f-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="97d5f-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97d5f-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="97d5f-139">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="97d5f-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="97d5f-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="97d5f-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="97d5f-141">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="97d5f-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="97d5f-142">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="97d5f-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="97d5f-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="97d5f-143">-EdgeNodeSize</span></span>
<span data-ttu-id="97d5f-144">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="97d5f-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="97d5f-145">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="97d5f-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="97d5f-146">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="97d5f-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="97d5f-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="97d5f-147">-HeadNodeSize</span></span>
<span data-ttu-id="97d5f-148">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="97d5f-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="97d5f-149">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="97d5f-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="97d5f-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="97d5f-150">-HiveMetastore</span></span>
<span data-ttu-id="97d5f-151">指定要儲存 Hive 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="97d5f-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="97d5f-152">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97d5f-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="97d5f-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="97d5f-153">-ObjectId</span></span>
<span data-ttu-id="97d5f-154">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="97d5f-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="97d5f-155">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="97d5f-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="97d5f-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="97d5f-156">-OozieMetastore</span></span>
<span data-ttu-id="97d5f-157">指定要儲存 Oozie 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="97d5f-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="97d5f-158">您也可以使用 **AzHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97d5f-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="97d5f-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="97d5f-159">-WorkerNodeSize</span></span>
<span data-ttu-id="97d5f-160">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="97d5f-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="97d5f-161">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="97d5f-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="97d5f-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="97d5f-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="97d5f-163">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="97d5f-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="97d5f-164">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="97d5f-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="97d5f-165">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="97d5f-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="97d5f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d5f-166">CommonParameters</span></span>
<span data-ttu-id="97d5f-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97d5f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d5f-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97d5f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d5f-169">輸入</span><span class="sxs-lookup"><span data-stu-id="97d5f-169">INPUTS</span></span>

### <span data-ttu-id="97d5f-170">所有</span><span class="sxs-lookup"><span data-stu-id="97d5f-170">None</span></span>

## <span data-ttu-id="97d5f-171">輸出</span><span class="sxs-lookup"><span data-stu-id="97d5f-171">OUTPUTS</span></span>

### <span data-ttu-id="97d5f-172">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="97d5f-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="97d5f-173">筆記</span><span class="sxs-lookup"><span data-stu-id="97d5f-173">NOTES</span></span>

## <span data-ttu-id="97d5f-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="97d5f-174">RELATED LINKS</span></span>

[<span data-ttu-id="97d5f-175">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="97d5f-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


