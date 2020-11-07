---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626291"
---
# <span data-ttu-id="fac62-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fac62-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="fac62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fac62-102">SYNOPSIS</span></span>
<span data-ttu-id="fac62-103">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac62-104">句法</span><span class="sxs-lookup"><span data-stu-id="fac62-104">SYNTAX</span></span>

### <span data-ttu-id="fac62-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="fac62-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fac62-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="fac62-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fac62-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="fac62-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fac62-108">說明</span><span class="sxs-lookup"><span data-stu-id="fac62-108">DESCRIPTION</span></span>
<span data-ttu-id="fac62-109">New-AzureHDInsightCluster 會使用指定的參數或使用 New-AzureRmHDInsightClusterConfig Cmdlet 建立的設定物件來建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="fac62-110">示例</span><span class="sxs-lookup"><span data-stu-id="fac62-110">EXAMPLES</span></span>

### <span data-ttu-id="fac62-111">--------------------------範例1：建立 Azure HDInsight 群集--------------------------</span><span class="sxs-lookup"><span data-stu-id="fac62-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="fac62-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="fac62-112">@{paragraph=PS C:\\\>}</span></span>









```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
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

<span data-ttu-id="fac62-113">這個命令會在目前的訂閱中建立群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="fac62-114">參數</span><span class="sxs-lookup"><span data-stu-id="fac62-114">PARAMETERS</span></span>

### <span data-ttu-id="fac62-115">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="fac62-115">-AadTenantId</span></span>
<span data-ttu-id="fac62-116">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="fac62-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fac62-117">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="fac62-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="fac62-118">指定群集的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fac62-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="fac62-119">您也可以使用 Add-AzureRmHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="fac62-120">-CertificateFileContents</span></span>
<span data-ttu-id="fac62-121">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="fac62-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="fac62-122">-CertificateFilePath</span></span>
<span data-ttu-id="fac62-123">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="fac62-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="fac62-124">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="fac62-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fac62-125">-CertificatePassword</span></span>
<span data-ttu-id="fac62-126">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="fac62-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="fac62-127">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="fac62-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fac62-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fac62-128">-ClusterName</span></span>
<span data-ttu-id="fac62-129">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="fac62-129">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="fac62-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="fac62-131">指定群集的輔助角色節點數。</span><span class="sxs-lookup"><span data-stu-id="fac62-131">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="fac62-132">-ClusterTier</span></span>
<span data-ttu-id="fac62-133">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="fac62-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="fac62-134">根據預設，這是標準的。</span><span class="sxs-lookup"><span data-stu-id="fac62-134">By default, this is Standard.</span></span>
<span data-ttu-id="fac62-135">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="fac62-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="fac62-136">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="fac62-136">-ClusterType</span></span>
<span data-ttu-id="fac62-137">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="fac62-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="fac62-138">選項包括： Hadoop、HBase、風暴、Spark</span><span class="sxs-lookup"><span data-stu-id="fac62-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="fac62-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="fac62-139">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-140">-Config</span><span class="sxs-lookup"><span data-stu-id="fac62-140">-Config</span></span>
<span data-ttu-id="fac62-141">指定要用來建立群集的群集物件。</span><span class="sxs-lookup"><span data-stu-id="fac62-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="fac62-142">您可以使用 New-AzureRmHDInsightClusterConfig Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="fac62-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-143">-配置</span><span class="sxs-lookup"><span data-stu-id="fac62-143">-Configurations</span></span>
<span data-ttu-id="fac62-144">指定此 HDInsight 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="fac62-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="fac62-145">您也可以使用 Add-AzureRmHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fac62-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="fac62-147">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="fac62-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fac62-148">您也可以使用 Set-AzureRmHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fac62-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="fac62-150">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fac62-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fac62-151">您也可以使用 Set-AzureRmHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fac62-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="fac62-153">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="fac62-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="fac62-154">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="fac62-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="fac62-155">如果沒有指定，則預設為 AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="fac62-155">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fac62-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="fac62-157">指定 HDInsight 群集將使用之預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fac62-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="fac62-158">您也可以使用 Set-AzureRmHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="fac62-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="fac62-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="fac62-160">指定在 Data Lake Store 帳戶中，HDInsight 群集將用來做為預設 filesystem 的路徑-前置詞。</span><span class="sxs-lookup"><span data-stu-id="fac62-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="fac62-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="fac62-161">-EdgeNodeSize</span></span>
<span data-ttu-id="fac62-162">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="fac62-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="fac62-163">使用 Get-AzureRmVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fac62-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="fac62-164">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="fac62-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="fac62-165">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="fac62-165">-HeadNodeSize</span></span>
<span data-ttu-id="fac62-166">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="fac62-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="fac62-167">使用 Get-AzureRmVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fac62-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="fac62-168">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="fac62-168">-HiveMetastore</span></span>
<span data-ttu-id="fac62-169">指定要儲存 Hive 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="fac62-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="fac62-170">您也可以使用 Add-AzureRmHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="fac62-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="fac62-171">-HttpCredential</span></span>
<span data-ttu-id="fac62-172">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="fac62-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-173">-位置</span><span class="sxs-lookup"><span data-stu-id="fac62-173">-Location</span></span>
<span data-ttu-id="fac62-174">指定群集的位置。</span><span class="sxs-lookup"><span data-stu-id="fac62-174">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fac62-175">-ObjectId</span></span>
<span data-ttu-id="fac62-176">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="fac62-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="fac62-177">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="fac62-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="fac62-178">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="fac62-178">-OozieMetastore</span></span>
<span data-ttu-id="fac62-179">指定 SQL 資料庫以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fac62-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="fac62-180">您也可以使用 Add-AzureRmHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="fac62-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="fac62-181">-OSType</span></span>
<span data-ttu-id="fac62-182">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="fac62-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="fac62-183">選項包括： Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="fac62-183">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-184">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="fac62-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="fac62-185">指定遠端桌面通訊協定的到期日（例如 DateTime 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="fac62-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="fac62-186">-RdpCredential</span></span>
<span data-ttu-id="fac62-187">為群集指定遠端桌面 (RDP) 認證。</span><span class="sxs-lookup"><span data-stu-id="fac62-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="fac62-188">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-188">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac62-189">-ResourceGroupName</span></span>
<span data-ttu-id="fac62-190">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fac62-190">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-191">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="fac62-191">-ScriptActions</span></span>
<span data-ttu-id="fac62-192">指定在群集建立結束時，要在群集上執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="fac62-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="fac62-193">您也可以使用 [載入 AzureRmHDInsightScriptAction]。</span><span class="sxs-lookup"><span data-stu-id="fac62-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="fac62-194">-SecurityProfile</span></span>
<span data-ttu-id="fac62-195">指定用來建立安全群集的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="fac62-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="fac62-196">您也可以使用 Add-AzureRmHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fac62-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="fac62-197">-SshCredential</span></span>
<span data-ttu-id="fac62-198">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="fac62-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="fac62-199">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-199">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac62-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fac62-200">-SshPublicKey</span></span>
<span data-ttu-id="fac62-201">指定要用於 SSH 連接的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="fac62-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="fac62-202">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="fac62-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="fac62-203">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fac62-203">-SubnetName</span></span>
<span data-ttu-id="fac62-204">在已選取的群集虛擬網路中，指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="fac62-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="fac62-205">-版本</span><span class="sxs-lookup"><span data-stu-id="fac62-205">-Version</span></span>
<span data-ttu-id="fac62-206">指定 HDInsight 群集的 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="fac62-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="fac62-207">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fac62-207">-VirtualNetworkId</span></span>
<span data-ttu-id="fac62-208">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="fac62-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="fac62-209">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="fac62-209">-WorkerNodeSize</span></span>
<span data-ttu-id="fac62-210">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="fac62-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="fac62-211">使用 Get-AzureRmVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fac62-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="fac62-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="fac62-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="fac62-213">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="fac62-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="fac62-214">使用 Get-AzureRmVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="fac62-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="fac62-215">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="fac62-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="fac62-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac62-216">-DefaultProfile</span></span>
<span data-ttu-id="fac62-217">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fac62-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fac62-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac62-218">CommonParameters</span></span>
<span data-ttu-id="fac62-219">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fac62-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac62-220">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fac62-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac62-221">輸入</span><span class="sxs-lookup"><span data-stu-id="fac62-221">INPUTS</span></span>

### <span data-ttu-id="fac62-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="fac62-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="fac62-223">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fac62-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="fac62-224">輸出</span><span class="sxs-lookup"><span data-stu-id="fac62-224">OUTPUTS</span></span>

### <span data-ttu-id="fac62-225">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="fac62-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="fac62-226">筆記</span><span class="sxs-lookup"><span data-stu-id="fac62-226">NOTES</span></span>
<span data-ttu-id="fac62-227">關鍵字： azure，azurerm，arm，資源，管理，管理員，hadoop，hdinsight，hd，洞察力</span><span class="sxs-lookup"><span data-stu-id="fac62-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="fac62-228">相關連結</span><span class="sxs-lookup"><span data-stu-id="fac62-228">RELATED LINKS</span></span>

[<span data-ttu-id="fac62-229">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="fac62-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

