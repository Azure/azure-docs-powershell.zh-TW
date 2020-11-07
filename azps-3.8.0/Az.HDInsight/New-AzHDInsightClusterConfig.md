---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799197"
---
# <span data-ttu-id="54939-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="54939-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="54939-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54939-102">SYNOPSIS</span></span>
<span data-ttu-id="54939-103">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="54939-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="54939-104">句法</span><span class="sxs-lookup"><span data-stu-id="54939-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54939-105">說明</span><span class="sxs-lookup"><span data-stu-id="54939-105">DESCRIPTION</span></span>
<span data-ttu-id="54939-106">**新的-AzHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。</span><span class="sxs-lookup"><span data-stu-id="54939-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="54939-107">示例</span><span class="sxs-lookup"><span data-stu-id="54939-107">EXAMPLES</span></span>

### <span data-ttu-id="54939-108">範例1：建立群集設定物件</span><span class="sxs-lookup"><span data-stu-id="54939-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="54939-109">這個命令會建立群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="54939-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="54939-110">參數</span><span class="sxs-lookup"><span data-stu-id="54939-110">PARAMETERS</span></span>

### <span data-ttu-id="54939-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="54939-111">-AadTenantId</span></span>
<span data-ttu-id="54939-112">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="54939-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="54939-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54939-113">-ApplicationId</span></span>
<span data-ttu-id="54939-114">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="54939-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="54939-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="54939-115">-CertificateFileContents</span></span>
<span data-ttu-id="54939-116">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="54939-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="54939-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="54939-117">-CertificateFilePath</span></span>
<span data-ttu-id="54939-118">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="54939-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="54939-119">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="54939-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="54939-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="54939-120">-CertificatePassword</span></span>
<span data-ttu-id="54939-121">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="54939-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="54939-122">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="54939-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="54939-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="54939-123">-ClusterTier</span></span>
<span data-ttu-id="54939-124">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="54939-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="54939-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="54939-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54939-126">標準</span><span class="sxs-lookup"><span data-stu-id="54939-126">Standard</span></span>
- <span data-ttu-id="54939-127">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="54939-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="54939-128">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="54939-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="54939-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="54939-129">-ClusterType</span></span>
<span data-ttu-id="54939-130">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="54939-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="54939-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="54939-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54939-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="54939-132">Hadoop</span></span>
- <span data-ttu-id="54939-133">HBase</span><span class="sxs-lookup"><span data-stu-id="54939-133">HBase</span></span>
- <span data-ttu-id="54939-134">暴</span><span class="sxs-lookup"><span data-stu-id="54939-134">Storm</span></span>
- <span data-ttu-id="54939-135">Spark</span><span class="sxs-lookup"><span data-stu-id="54939-135">Spark</span></span>
- <span data-ttu-id="54939-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="54939-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="54939-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="54939-137">Kafka</span></span>
- <span data-ttu-id="54939-138">RServer</span><span class="sxs-lookup"><span data-stu-id="54939-138">RServer</span></span>

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

### <span data-ttu-id="54939-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54939-139">-DefaultProfile</span></span>
<span data-ttu-id="54939-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="54939-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54939-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="54939-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="54939-142">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="54939-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="54939-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="54939-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="54939-144">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="54939-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="54939-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="54939-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="54939-146">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="54939-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="54939-147">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="54939-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="54939-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="54939-148">-EdgeNodeSize</span></span>
<span data-ttu-id="54939-149">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="54939-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="54939-150">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="54939-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="54939-151">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="54939-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="54939-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="54939-152">-HeadNodeSize</span></span>
<span data-ttu-id="54939-153">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="54939-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="54939-154">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="54939-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="54939-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="54939-155">-HiveMetastore</span></span>
<span data-ttu-id="54939-156">指定要儲存 Hive 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="54939-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="54939-157">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54939-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="54939-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="54939-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="54939-159">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="54939-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="54939-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54939-160">-ObjectId</span></span>
<span data-ttu-id="54939-161">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="54939-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="54939-162">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="54939-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="54939-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="54939-163">-OozieMetastore</span></span>
<span data-ttu-id="54939-164">指定要儲存 Oozie 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="54939-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="54939-165">您也可以使用 **AzHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54939-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="54939-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="54939-166">-WorkerNodeSize</span></span>
<span data-ttu-id="54939-167">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="54939-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="54939-168">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="54939-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="54939-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="54939-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="54939-170">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="54939-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="54939-171">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="54939-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="54939-172">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="54939-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="54939-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54939-173">CommonParameters</span></span>
<span data-ttu-id="54939-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54939-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54939-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="54939-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54939-176">輸入</span><span class="sxs-lookup"><span data-stu-id="54939-176">INPUTS</span></span>

### <span data-ttu-id="54939-177">所有</span><span class="sxs-lookup"><span data-stu-id="54939-177">None</span></span>

## <span data-ttu-id="54939-178">輸出</span><span class="sxs-lookup"><span data-stu-id="54939-178">OUTPUTS</span></span>

### <span data-ttu-id="54939-179">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="54939-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="54939-180">筆記</span><span class="sxs-lookup"><span data-stu-id="54939-180">NOTES</span></span>

## <span data-ttu-id="54939-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="54939-181">RELATED LINKS</span></span>

[<span data-ttu-id="54939-182">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="54939-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


