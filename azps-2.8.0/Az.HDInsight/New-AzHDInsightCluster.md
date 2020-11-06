---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612292"
---
# <span data-ttu-id="5181b-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5181b-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="5181b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5181b-102">SYNOPSIS</span></span>
<span data-ttu-id="5181b-103">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="5181b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5181b-104">SYNTAX</span></span>

### <span data-ttu-id="5181b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="5181b-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5181b-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="5181b-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5181b-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="5181b-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5181b-108">說明</span><span class="sxs-lookup"><span data-stu-id="5181b-108">DESCRIPTION</span></span>
<span data-ttu-id="5181b-109">New-AzHDInsightCluster 會使用指定的參數或使用 New-AzHDInsightClusterConfig Cmdlet 建立的設定物件來建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="5181b-110">示例</span><span class="sxs-lookup"><span data-stu-id="5181b-110">EXAMPLES</span></span>

### <span data-ttu-id="5181b-111">範例1：建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="5181b-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="5181b-112">這個命令會在目前的訂閱中建立群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="5181b-113">參數</span><span class="sxs-lookup"><span data-stu-id="5181b-113">PARAMETERS</span></span>

### <span data-ttu-id="5181b-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="5181b-114">-AadTenantId</span></span>
<span data-ttu-id="5181b-115">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="5181b-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5181b-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5181b-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="5181b-117">指定群集的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5181b-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="5181b-118">您也可以使用 Add-AzHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="5181b-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="5181b-119">-CertificateFileContents</span></span>
<span data-ttu-id="5181b-120">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="5181b-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5181b-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="5181b-121">-CertificateFilePath</span></span>
<span data-ttu-id="5181b-122">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5181b-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="5181b-123">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5181b-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5181b-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5181b-124">-CertificatePassword</span></span>
<span data-ttu-id="5181b-125">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="5181b-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="5181b-126">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5181b-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5181b-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5181b-127">-ClusterName</span></span>
<span data-ttu-id="5181b-128">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5181b-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5181b-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="5181b-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="5181b-130">指定群集的輔助角色節點數。</span><span class="sxs-lookup"><span data-stu-id="5181b-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="5181b-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="5181b-131">-ClusterTier</span></span>
<span data-ttu-id="5181b-132">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="5181b-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="5181b-133">根據預設，這是標準的。</span><span class="sxs-lookup"><span data-stu-id="5181b-133">By default, this is Standard.</span></span>
<span data-ttu-id="5181b-134">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="5181b-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="5181b-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="5181b-135">-ClusterType</span></span>
<span data-ttu-id="5181b-136">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="5181b-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="5181b-137">選項包括： Hadoop、HBase、風暴、Spark</span><span class="sxs-lookup"><span data-stu-id="5181b-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="5181b-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="5181b-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="5181b-139">-Config</span><span class="sxs-lookup"><span data-stu-id="5181b-139">-Config</span></span>
<span data-ttu-id="5181b-140">指定要用來建立群集的群集物件。</span><span class="sxs-lookup"><span data-stu-id="5181b-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="5181b-141">您可以使用 New-AzHDInsightClusterConfig Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="5181b-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="5181b-142">-配置</span><span class="sxs-lookup"><span data-stu-id="5181b-142">-Configurations</span></span>
<span data-ttu-id="5181b-143">指定此 HDInsight 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="5181b-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="5181b-144">您也可以使用 Add-AzHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="5181b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5181b-145">-DefaultProfile</span></span>
<span data-ttu-id="5181b-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5181b-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5181b-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5181b-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="5181b-148">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="5181b-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="5181b-149">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="5181b-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5181b-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="5181b-151">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5181b-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="5181b-152">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="5181b-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5181b-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="5181b-154">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="5181b-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="5181b-155">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="5181b-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="5181b-156">如果沒有指定，則預設為 AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="5181b-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="5181b-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5181b-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="5181b-158">指定 HDInsight 群集將使用之預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5181b-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="5181b-159">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="5181b-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="5181b-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="5181b-161">指定在 Data Lake Store 帳戶中，HDInsight 群集將用來做為預設 filesystem 的路徑-前置詞。</span><span class="sxs-lookup"><span data-stu-id="5181b-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="5181b-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="5181b-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="5181b-163">指定群集中輔助角色節點角色的磁片數。</span><span class="sxs-lookup"><span data-stu-id="5181b-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5181b-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="5181b-164">-EdgeNodeSize</span></span>
<span data-ttu-id="5181b-165">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5181b-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="5181b-166">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5181b-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="5181b-167">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="5181b-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="5181b-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="5181b-168">-HeadNodeSize</span></span>
<span data-ttu-id="5181b-169">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5181b-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="5181b-170">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5181b-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="5181b-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="5181b-171">-HiveMetastore</span></span>
<span data-ttu-id="5181b-172">指定要儲存 Hive 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5181b-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="5181b-173">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="5181b-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5181b-174">-HttpCredential</span></span>
<span data-ttu-id="5181b-175">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="5181b-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="5181b-176">-位置</span><span class="sxs-lookup"><span data-stu-id="5181b-176">-Location</span></span>
<span data-ttu-id="5181b-177">指定群集的位置。</span><span class="sxs-lookup"><span data-stu-id="5181b-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="5181b-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5181b-178">-ObjectId</span></span>
<span data-ttu-id="5181b-179">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="5181b-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="5181b-180">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="5181b-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="5181b-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="5181b-181">-OozieMetastore</span></span>
<span data-ttu-id="5181b-182">指定 SQL 資料庫以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5181b-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="5181b-183">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="5181b-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="5181b-184">-OSType</span></span>
<span data-ttu-id="5181b-185">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5181b-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="5181b-186">選項包括： Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="5181b-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="5181b-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="5181b-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="5181b-188">指定遠端桌面通訊協定的到期日（例如 DateTime 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="5181b-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="5181b-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="5181b-189">-RdpCredential</span></span>
<span data-ttu-id="5181b-190">為群集指定遠端桌面 (RDP) 認證。</span><span class="sxs-lookup"><span data-stu-id="5181b-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="5181b-191">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="5181b-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5181b-192">-ResourceGroupName</span></span>
<span data-ttu-id="5181b-193">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5181b-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5181b-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="5181b-194">-ScriptActions</span></span>
<span data-ttu-id="5181b-195">指定在群集建立結束時，要在群集上執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="5181b-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="5181b-196">您也可以使用 [載入 AzHDInsightScriptAction]。</span><span class="sxs-lookup"><span data-stu-id="5181b-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="5181b-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="5181b-197">-SecurityProfile</span></span>
<span data-ttu-id="5181b-198">指定用來建立安全群集的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="5181b-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="5181b-199">您也可以使用 Add-AzHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5181b-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="5181b-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="5181b-200">-SshCredential</span></span>
<span data-ttu-id="5181b-201">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="5181b-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="5181b-202">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="5181b-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5181b-203">-SshPublicKey</span></span>
<span data-ttu-id="5181b-204">指定要用於 SSH 連接的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="5181b-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="5181b-205">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="5181b-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="5181b-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5181b-206">-SubnetName</span></span>
<span data-ttu-id="5181b-207">在已選取的群集虛擬網路中，指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="5181b-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="5181b-208">-版本</span><span class="sxs-lookup"><span data-stu-id="5181b-208">-Version</span></span>
<span data-ttu-id="5181b-209">指定 HDInsight 群集的 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="5181b-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="5181b-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5181b-210">-VirtualNetworkId</span></span>
<span data-ttu-id="5181b-211">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="5181b-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="5181b-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="5181b-212">-WorkerNodeSize</span></span>
<span data-ttu-id="5181b-213">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5181b-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="5181b-214">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5181b-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="5181b-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="5181b-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="5181b-216">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="5181b-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="5181b-217">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5181b-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="5181b-218">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="5181b-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="5181b-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5181b-219">CommonParameters</span></span>
<span data-ttu-id="5181b-220">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5181b-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5181b-221">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5181b-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5181b-222">輸入</span><span class="sxs-lookup"><span data-stu-id="5181b-222">INPUTS</span></span>

### <span data-ttu-id="5181b-223">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="5181b-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5181b-224">輸出</span><span class="sxs-lookup"><span data-stu-id="5181b-224">OUTPUTS</span></span>

### <span data-ttu-id="5181b-225">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="5181b-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="5181b-226">筆記</span><span class="sxs-lookup"><span data-stu-id="5181b-226">NOTES</span></span>
<span data-ttu-id="5181b-227">關鍵字： azure，azurerm，arm，資源，管理，管理員，hadoop，hdinsight，hd，洞察力</span><span class="sxs-lookup"><span data-stu-id="5181b-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="5181b-228">相關連結</span><span class="sxs-lookup"><span data-stu-id="5181b-228">RELATED LINKS</span></span>

[<span data-ttu-id="5181b-229">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5181b-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

