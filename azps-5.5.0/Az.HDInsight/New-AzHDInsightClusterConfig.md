---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139150"
---
# <span data-ttu-id="c3790-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c3790-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="c3790-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3790-102">SYNOPSIS</span></span>
<span data-ttu-id="c3790-103">建立描述 Azure HDInsight 群集設定的非持久化群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="c3790-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c3790-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3790-104">SYNTAX</span></span>

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

## <span data-ttu-id="c3790-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3790-105">DESCRIPTION</span></span>
<span data-ttu-id="c3790-106">**新的-AzHDInsightClusterConfig** Cmdlet 會建立一個描述 Azure HDInsight 群集設定的非持久物件。</span><span class="sxs-lookup"><span data-stu-id="c3790-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c3790-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3790-107">EXAMPLES</span></span>

### <span data-ttu-id="c3790-108">範例1：建立群集設定物件</span><span class="sxs-lookup"><span data-stu-id="c3790-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="c3790-109">這個命令會建立群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="c3790-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="c3790-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3790-110">PARAMETERS</span></span>

### <span data-ttu-id="c3790-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c3790-111">-AadTenantId</span></span>
<span data-ttu-id="c3790-112">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3790-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c3790-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c3790-113">-ApplicationId</span></span>
<span data-ttu-id="c3790-114">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3790-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="c3790-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c3790-115">-AssignedIdentity</span></span>
<span data-ttu-id="c3790-116">取得或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c3790-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="c3790-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c3790-117">-CertificateFileContents</span></span>
<span data-ttu-id="c3790-118">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="c3790-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c3790-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c3790-119">-CertificateFilePath</span></span>
<span data-ttu-id="c3790-120">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c3790-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c3790-121">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c3790-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c3790-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c3790-122">-CertificatePassword</span></span>
<span data-ttu-id="c3790-123">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="c3790-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c3790-124">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c3790-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c3790-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c3790-125">-ClusterTier</span></span>
<span data-ttu-id="c3790-126">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="c3790-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c3790-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c3790-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3790-128">標準</span><span class="sxs-lookup"><span data-stu-id="c3790-128">Standard</span></span>
- <span data-ttu-id="c3790-129">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="c3790-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="c3790-130">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="c3790-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c3790-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c3790-131">-ClusterType</span></span>
<span data-ttu-id="c3790-132">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="c3790-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c3790-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c3790-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3790-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="c3790-134">Hadoop</span></span>
- <span data-ttu-id="c3790-135">HBase</span><span class="sxs-lookup"><span data-stu-id="c3790-135">HBase</span></span>
- <span data-ttu-id="c3790-136">暴</span><span class="sxs-lookup"><span data-stu-id="c3790-136">Storm</span></span>
- <span data-ttu-id="c3790-137">Spark</span><span class="sxs-lookup"><span data-stu-id="c3790-137">Spark</span></span>
- <span data-ttu-id="c3790-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="c3790-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="c3790-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="c3790-139">Kafka</span></span>
- <span data-ttu-id="c3790-140">RServer</span><span class="sxs-lookup"><span data-stu-id="c3790-140">RServer</span></span>

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

### <span data-ttu-id="c3790-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3790-141">-DefaultProfile</span></span>
<span data-ttu-id="c3790-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c3790-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3790-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c3790-143">-EdgeNodeSize</span></span>
<span data-ttu-id="c3790-144">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c3790-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c3790-145">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c3790-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c3790-146">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="c3790-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c3790-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c3790-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="c3790-148">取得或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="c3790-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="c3790-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c3790-149">-EncryptionAtHost</span></span>
<span data-ttu-id="c3790-150">取得或設定標誌，以指出是否要在主機上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3790-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="c3790-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="c3790-151">-EncryptionInTransit</span></span>
<span data-ttu-id="c3790-152">取得或設定標誌，以指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3790-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="c3790-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c3790-153">-EncryptionKeyName</span></span>
<span data-ttu-id="c3790-154">取得或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="c3790-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="c3790-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c3790-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c3790-156">取得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="c3790-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="c3790-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="c3790-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="c3790-158">取得或設定加密 vault uri。</span><span class="sxs-lookup"><span data-stu-id="c3790-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="c3790-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c3790-159">-HeadNodeSize</span></span>
<span data-ttu-id="c3790-160">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c3790-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c3790-161">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c3790-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c3790-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="c3790-162">-HiveMetastore</span></span>
<span data-ttu-id="c3790-163">指定要儲存 Hive 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="c3790-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="c3790-164">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3790-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c3790-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c3790-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="c3790-166">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="c3790-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="c3790-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c3790-167">-ObjectId</span></span>
<span data-ttu-id="c3790-168">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="c3790-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c3790-169">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c3790-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c3790-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c3790-170">-OozieMetastore</span></span>
<span data-ttu-id="c3790-171">指定要儲存 Oozie 中繼資料的 metastore。</span><span class="sxs-lookup"><span data-stu-id="c3790-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="c3790-172">您也可以使用 **AzHDInsightMetastore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3790-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="c3790-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c3790-173">-StorageAccountKey</span></span>
<span data-ttu-id="c3790-174">取得或設定儲存空間帳戶訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="c3790-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="c3790-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c3790-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="c3790-176">取得或設定儲存空間帳戶資源 id。</span><span class="sxs-lookup"><span data-stu-id="c3790-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="c3790-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c3790-177">-StorageAccountType</span></span>
<span data-ttu-id="c3790-178">取得或設定預設儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="c3790-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="c3790-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c3790-179">-WorkerNodeSize</span></span>
<span data-ttu-id="c3790-180">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c3790-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c3790-181">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c3790-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c3790-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c3790-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c3790-183">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c3790-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c3790-184">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c3790-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c3790-185">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="c3790-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c3790-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3790-186">CommonParameters</span></span>
<span data-ttu-id="c3790-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3790-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3790-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3790-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3790-189">輸入</span><span class="sxs-lookup"><span data-stu-id="c3790-189">INPUTS</span></span>

### <span data-ttu-id="c3790-190">所有</span><span class="sxs-lookup"><span data-stu-id="c3790-190">None</span></span>

## <span data-ttu-id="c3790-191">輸出</span><span class="sxs-lookup"><span data-stu-id="c3790-191">OUTPUTS</span></span>

### <span data-ttu-id="c3790-192">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c3790-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c3790-193">筆記</span><span class="sxs-lookup"><span data-stu-id="c3790-193">NOTES</span></span>

## <span data-ttu-id="c3790-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3790-194">RELATED LINKS</span></span>

[<span data-ttu-id="c3790-195">附加 AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c3790-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


