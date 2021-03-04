---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: b5ae1de58a7c3862379e73e852d7b367063c3629
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916554"
---
# <span data-ttu-id="e96f7-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e96f7-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="e96f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e96f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e96f7-103">建立描述 Azure HDInsight 集區組配置的非持續型集組組物件。</span><span class="sxs-lookup"><span data-stu-id="e96f7-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e96f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="e96f7-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e96f7-105">描述</span><span class="sxs-lookup"><span data-stu-id="e96f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e96f7-106">**New-AzHDInsightClusterConfig** Cmdlet 會建立描述 Azure HDInsight 叢集組配置的非持續物件。</span><span class="sxs-lookup"><span data-stu-id="e96f7-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e96f7-107">例子</span><span class="sxs-lookup"><span data-stu-id="e96f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e96f7-108">範例 1：建立組組物件</span><span class="sxs-lookup"><span data-stu-id="e96f7-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="e96f7-109">此命令會建立一個組組物件。</span><span class="sxs-lookup"><span data-stu-id="e96f7-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="e96f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e96f7-110">PARAMETERS</span></span>

### <span data-ttu-id="e96f7-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e96f7-111">-AadTenantId</span></span>
<span data-ttu-id="e96f7-112">指定存取 Azure Data Lake Store 時將會使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96f7-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e96f7-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e96f7-113">-ApplicationId</span></span>
<span data-ttu-id="e96f7-114">取得或設定存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96f7-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="e96f7-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e96f7-115">-AssignedIdentity</span></span>
<span data-ttu-id="e96f7-116">獲取或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e96f7-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="e96f7-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e96f7-117">-CertificateFileContents</span></span>
<span data-ttu-id="e96f7-118">指定存取 Azure Data Lake Store 時將使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="e96f7-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e96f7-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e96f7-119">-CertificateFilePath</span></span>
<span data-ttu-id="e96f7-120">指定要用來驗證為服務主體之憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e96f7-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e96f7-121">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="e96f7-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e96f7-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e96f7-122">-CertificatePassword</span></span>
<span data-ttu-id="e96f7-123">指定要用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="e96f7-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e96f7-124">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="e96f7-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e96f7-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e96f7-125">-ClusterTier</span></span>
<span data-ttu-id="e96f7-126">指定 HDInsight 集區層級。</span><span class="sxs-lookup"><span data-stu-id="e96f7-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e96f7-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96f7-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e96f7-128">標準</span><span class="sxs-lookup"><span data-stu-id="e96f7-128">Standard</span></span>
- <span data-ttu-id="e96f7-129">Premium 預設值為 Standard。</span><span class="sxs-lookup"><span data-stu-id="e96f7-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="e96f7-130">進一層只能與 Linux 系列一起使用，而且能使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="e96f7-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="e96f7-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e96f7-131">-ClusterType</span></span>
<span data-ttu-id="e96f7-132">指定要建立之組群的類型。</span><span class="sxs-lookup"><span data-stu-id="e96f7-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e96f7-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e96f7-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e96f7-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="e96f7-134">Hadoop</span></span>
- <span data-ttu-id="e96f7-135">HBase</span><span class="sxs-lookup"><span data-stu-id="e96f7-135">HBase</span></span>
- <span data-ttu-id="e96f7-136">風暴</span><span class="sxs-lookup"><span data-stu-id="e96f7-136">Storm</span></span>
- <span data-ttu-id="e96f7-137">火花</span><span class="sxs-lookup"><span data-stu-id="e96f7-137">Spark</span></span>
- <span data-ttu-id="e96f7-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="e96f7-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="e96f7-139">卡 夫 卡</span><span class="sxs-lookup"><span data-stu-id="e96f7-139">Kafka</span></span>
- <span data-ttu-id="e96f7-140">RServer</span><span class="sxs-lookup"><span data-stu-id="e96f7-140">RServer</span></span>

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

### <span data-ttu-id="e96f7-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96f7-141">-DefaultProfile</span></span>
<span data-ttu-id="e96f7-142">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e96f7-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e96f7-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e96f7-143">-EdgeNodeSize</span></span>
<span data-ttu-id="e96f7-144">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e96f7-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e96f7-145">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="e96f7-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e96f7-146">此參數僅適用于 RServer 群。</span><span class="sxs-lookup"><span data-stu-id="e96f7-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e96f7-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e96f7-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e96f7-148">獲取或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="e96f7-148">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f7-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e96f7-149">-EncryptionAtHost</span></span>
<span data-ttu-id="e96f7-150">套用或設定旗標，指出是否要在主機啟用加密。</span><span class="sxs-lookup"><span data-stu-id="e96f7-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f7-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e96f7-151">-EncryptionInTransit</span></span>
<span data-ttu-id="e96f7-152">套用或設定旗標，指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="e96f7-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f7-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e96f7-153">-EncryptionKeyName</span></span>
<span data-ttu-id="e96f7-154">獲取或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="e96f7-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="e96f7-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e96f7-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e96f7-156">獲得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="e96f7-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="e96f7-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e96f7-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="e96f7-158">獲取或設定加密庫 uri。</span><span class="sxs-lookup"><span data-stu-id="e96f7-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="e96f7-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e96f7-159">-HeadNodeSize</span></span>
<span data-ttu-id="e96f7-160">指定 Head 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e96f7-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e96f7-161">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="e96f7-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e96f7-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e96f7-162">-HiveMetastore</span></span>
<span data-ttu-id="e96f7-163">指定元存放區以儲存病毒中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e96f7-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="e96f7-164">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e96f7-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e96f7-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e96f7-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e96f7-166">獲得或設定最小支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="e96f7-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="e96f7-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e96f7-167">-ObjectId</span></span>
<span data-ttu-id="e96f7-168">指定代表該 (之 Azure AD 服務) GUID 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96f7-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e96f7-169">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="e96f7-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e96f7-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e96f7-170">-OozieMetastore</span></span>
<span data-ttu-id="e96f7-171">指定元存放區以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e96f7-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="e96f7-172">您也可以使用 **Add-AzHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e96f7-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="e96f7-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e96f7-173">-StorageAccountKey</span></span>
<span data-ttu-id="e96f7-174">取得或設定儲存空間帳戶便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e96f7-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="e96f7-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e96f7-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="e96f7-176">獲取或設定儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96f7-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="e96f7-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e96f7-177">-StorageAccountType</span></span>
<span data-ttu-id="e96f7-178">獲取或設定預設儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="e96f7-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96f7-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e96f7-179">-WorkerNodeSize</span></span>
<span data-ttu-id="e96f7-180">指定工作節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e96f7-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e96f7-181">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="e96f7-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e96f7-182">-KeeperkeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e96f7-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e96f7-183">指定資料管理節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e96f7-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e96f7-184">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="e96f7-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e96f7-185">此參數僅適用于 HBase 或暴風雪組。</span><span class="sxs-lookup"><span data-stu-id="e96f7-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e96f7-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96f7-186">CommonParameters</span></span>
<span data-ttu-id="e96f7-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e96f7-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96f7-188">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e96f7-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96f7-189">輸入</span><span class="sxs-lookup"><span data-stu-id="e96f7-189">INPUTS</span></span>

### <span data-ttu-id="e96f7-190">沒有</span><span class="sxs-lookup"><span data-stu-id="e96f7-190">None</span></span>

## <span data-ttu-id="e96f7-191">輸出</span><span class="sxs-lookup"><span data-stu-id="e96f7-191">OUTPUTS</span></span>

### <span data-ttu-id="e96f7-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e96f7-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e96f7-193">筆記</span><span class="sxs-lookup"><span data-stu-id="e96f7-193">NOTES</span></span>

## <span data-ttu-id="e96f7-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="e96f7-194">RELATED LINKS</span></span>

[<span data-ttu-id="e96f7-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e96f7-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


