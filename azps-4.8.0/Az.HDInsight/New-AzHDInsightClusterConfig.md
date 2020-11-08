---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970521"
---
# <span data-ttu-id="f64c4-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f64c4-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="f64c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f64c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f64c4-103">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f64c4-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f64c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f64c4-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f64c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="f64c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f64c4-106">**新的-AzHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。</span><span class="sxs-lookup"><span data-stu-id="f64c4-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f64c4-107">示例</span><span class="sxs-lookup"><span data-stu-id="f64c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f64c4-108">範例1：建立群集設定物件</span><span class="sxs-lookup"><span data-stu-id="f64c4-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="f64c4-109">這個命令會建立群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f64c4-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="f64c4-110">參數</span><span class="sxs-lookup"><span data-stu-id="f64c4-110">PARAMETERS</span></span>

### <span data-ttu-id="f64c4-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f64c4-111">-AadTenantId</span></span>
<span data-ttu-id="f64c4-112">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f64c4-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f64c4-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f64c4-113">-ApplicationId</span></span>
<span data-ttu-id="f64c4-114">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="f64c4-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f64c4-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f64c4-115">-AssignedIdentity</span></span>
<span data-ttu-id="f64c4-116">取得或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f64c4-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="f64c4-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f64c4-117">-CertificateFileContents</span></span>
<span data-ttu-id="f64c4-118">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="f64c4-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f64c4-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f64c4-119">-CertificateFilePath</span></span>
<span data-ttu-id="f64c4-120">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f64c4-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f64c4-121">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f64c4-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f64c4-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f64c4-122">-CertificatePassword</span></span>
<span data-ttu-id="f64c4-123">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="f64c4-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f64c4-124">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f64c4-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f64c4-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="f64c4-125">-ClusterTier</span></span>
<span data-ttu-id="f64c4-126">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="f64c4-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="f64c4-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f64c4-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f64c4-128">標準</span><span class="sxs-lookup"><span data-stu-id="f64c4-128">Standard</span></span>
- <span data-ttu-id="f64c4-129">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="f64c4-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="f64c4-130">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="f64c4-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="f64c4-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f64c4-131">-ClusterType</span></span>
<span data-ttu-id="f64c4-132">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="f64c4-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="f64c4-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f64c4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f64c4-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="f64c4-134">Hadoop</span></span>
- <span data-ttu-id="f64c4-135">HBase</span><span class="sxs-lookup"><span data-stu-id="f64c4-135">HBase</span></span>
- <span data-ttu-id="f64c4-136">暴</span><span class="sxs-lookup"><span data-stu-id="f64c4-136">Storm</span></span>
- <span data-ttu-id="f64c4-137">Spark</span><span class="sxs-lookup"><span data-stu-id="f64c4-137">Spark</span></span>
- <span data-ttu-id="f64c4-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="f64c4-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="f64c4-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="f64c4-139">Kafka</span></span>
- <span data-ttu-id="f64c4-140">RServer</span><span class="sxs-lookup"><span data-stu-id="f64c4-140">RServer</span></span>

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

### <span data-ttu-id="f64c4-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64c4-141">-DefaultProfile</span></span>
<span data-ttu-id="f64c4-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f64c4-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f64c4-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f64c4-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="f64c4-144">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="f64c4-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="f64c4-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f64c4-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="f64c4-146">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f64c4-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="f64c4-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f64c4-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="f64c4-148">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="f64c4-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="f64c4-149">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f64c4-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="f64c4-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="f64c4-150">-EdgeNodeSize</span></span>
<span data-ttu-id="f64c4-151">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f64c4-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="f64c4-152">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f64c4-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="f64c4-153">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="f64c4-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f64c4-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f64c4-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="f64c4-155">取得或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="f64c4-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="f64c4-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="f64c4-156">-EncryptionAtHost</span></span>
<span data-ttu-id="f64c4-157">取得或設定標誌，以指出是否要在主機上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="f64c4-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="f64c4-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="f64c4-158">-EncryptionInTransit</span></span>
<span data-ttu-id="f64c4-159">取得或設定標誌，以指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="f64c4-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="f64c4-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f64c4-160">-EncryptionKeyName</span></span>
<span data-ttu-id="f64c4-161">取得或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="f64c4-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="f64c4-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f64c4-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f64c4-163">取得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="f64c4-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="f64c4-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f64c4-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="f64c4-165">取得或設定加密 vault uri。</span><span class="sxs-lookup"><span data-stu-id="f64c4-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="f64c4-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="f64c4-166">-HeadNodeSize</span></span>
<span data-ttu-id="f64c4-167">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f64c4-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="f64c4-168">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f64c4-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f64c4-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="f64c4-169">-HiveMetastore</span></span>
<span data-ttu-id="f64c4-170">指定要儲存 Hive 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="f64c4-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="f64c4-171">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f64c4-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f64c4-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f64c4-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="f64c4-173">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="f64c4-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="f64c4-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f64c4-174">-ObjectId</span></span>
<span data-ttu-id="f64c4-175">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="f64c4-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f64c4-176">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f64c4-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f64c4-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="f64c4-177">-OozieMetastore</span></span>
<span data-ttu-id="f64c4-178">指定要儲存 Oozie 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="f64c4-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="f64c4-179">您也可以使用 **AzHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f64c4-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="f64c4-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="f64c4-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="f64c4-181">取得或設定公用網路的輸出存取類型。</span><span class="sxs-lookup"><span data-stu-id="f64c4-181">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64c4-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="f64c4-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="f64c4-183">取得或設定公用網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="f64c4-183">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64c4-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="f64c4-184">-WorkerNodeSize</span></span>
<span data-ttu-id="f64c4-185">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f64c4-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="f64c4-186">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f64c4-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f64c4-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="f64c4-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="f64c4-188">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f64c4-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="f64c4-189">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f64c4-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="f64c4-190">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="f64c4-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="f64c4-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64c4-191">CommonParameters</span></span>
<span data-ttu-id="f64c4-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f64c4-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64c4-193">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f64c4-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64c4-194">輸入</span><span class="sxs-lookup"><span data-stu-id="f64c4-194">INPUTS</span></span>

### <span data-ttu-id="f64c4-195">所有</span><span class="sxs-lookup"><span data-stu-id="f64c4-195">None</span></span>

## <span data-ttu-id="f64c4-196">輸出</span><span class="sxs-lookup"><span data-stu-id="f64c4-196">OUTPUTS</span></span>

### <span data-ttu-id="f64c4-197">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f64c4-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f64c4-198">筆記</span><span class="sxs-lookup"><span data-stu-id="f64c4-198">NOTES</span></span>

## <span data-ttu-id="f64c4-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="f64c4-199">RELATED LINKS</span></span>

[<span data-ttu-id="f64c4-200">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f64c4-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


