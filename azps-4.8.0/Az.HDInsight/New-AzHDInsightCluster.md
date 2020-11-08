---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970526"
---
# <span data-ttu-id="c2126-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2126-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="c2126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2126-102">SYNOPSIS</span></span>
<span data-ttu-id="c2126-103">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="c2126-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2126-104">SYNTAX</span></span>

### <span data-ttu-id="c2126-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c2126-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2126-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c2126-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2126-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c2126-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2126-108">說明</span><span class="sxs-lookup"><span data-stu-id="c2126-108">DESCRIPTION</span></span>
<span data-ttu-id="c2126-109">New-AzHDInsightCluster 會使用指定的參數或使用 New-AzHDInsightClusterConfig Cmdlet 建立的設定物件來建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c2126-110">示例</span><span class="sxs-lookup"><span data-stu-id="c2126-110">EXAMPLES</span></span>

### <span data-ttu-id="c2126-111">範例1：建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="c2126-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="c2126-112">這個命令會在目前的訂閱中建立群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="c2126-113">範例2：使用客戶管理的金鑰磁片加密建立群集</span><span class="sxs-lookup"><span data-stu-id="c2126-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="c2126-114">範例3：建立 Azure HDInsight 群集，以便在中轉時加密</span><span class="sxs-lookup"><span data-stu-id="c2126-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="c2126-115">範例4：使用私人連結功能建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="c2126-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="c2126-116">範例5：建立 Azure HDInsight 群集，在主機上啟用加密</span><span class="sxs-lookup"><span data-stu-id="c2126-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="c2126-117">範例6：建立可啟用自動縮放的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="c2126-118">參數</span><span class="sxs-lookup"><span data-stu-id="c2126-118">PARAMETERS</span></span>

### <span data-ttu-id="c2126-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c2126-119">-AadTenantId</span></span>
<span data-ttu-id="c2126-120">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2126-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2126-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c2126-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="c2126-122">指定群集的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c2126-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="c2126-123">您也可以使用 Add-AzHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="c2126-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c2126-124">-ApplicationId</span></span>
<span data-ttu-id="c2126-125">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2126-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="c2126-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c2126-126">-AssignedIdentity</span></span>
<span data-ttu-id="c2126-127">取得或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c2126-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="c2126-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2126-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="c2126-129">取得或設定自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="c2126-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2126-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c2126-130">-CertificateFileContents</span></span>
<span data-ttu-id="c2126-131">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="c2126-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2126-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c2126-132">-CertificateFilePath</span></span>
<span data-ttu-id="c2126-133">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c2126-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c2126-134">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c2126-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2126-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c2126-135">-CertificatePassword</span></span>
<span data-ttu-id="c2126-136">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="c2126-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c2126-137">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c2126-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2126-138">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2126-138">-ClusterName</span></span>
<span data-ttu-id="c2126-139">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c2126-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="c2126-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="c2126-141">指定群集的輔助角色節點數。</span><span class="sxs-lookup"><span data-stu-id="c2126-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="c2126-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c2126-142">-ClusterTier</span></span>
<span data-ttu-id="c2126-143">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="c2126-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c2126-144">根據預設，這是標準的。</span><span class="sxs-lookup"><span data-stu-id="c2126-144">By default, this is Standard.</span></span>
<span data-ttu-id="c2126-145">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="c2126-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c2126-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c2126-146">-ClusterType</span></span>
<span data-ttu-id="c2126-147">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="c2126-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c2126-148">選項包括： Hadoop、HBase、風暴、Spark、INTERACTIVEHIVE、Kafka 和 RServer</span><span class="sxs-lookup"><span data-stu-id="c2126-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="c2126-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c2126-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="c2126-150">-Config</span><span class="sxs-lookup"><span data-stu-id="c2126-150">-Config</span></span>
<span data-ttu-id="c2126-151">指定要用來建立群集的群集物件。</span><span class="sxs-lookup"><span data-stu-id="c2126-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="c2126-152">您可以使用 New-AzHDInsightClusterConfig Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="c2126-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="c2126-153">-配置</span><span class="sxs-lookup"><span data-stu-id="c2126-153">-Configurations</span></span>
<span data-ttu-id="c2126-154">指定此 HDInsight 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="c2126-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="c2126-155">您也可以使用 Add-AzHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="c2126-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2126-156">-DefaultProfile</span></span>
<span data-ttu-id="c2126-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c2126-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2126-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2126-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c2126-159">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2126-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c2126-160">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c2126-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2126-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c2126-162">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c2126-163">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c2126-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c2126-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="c2126-165">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="c2126-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="c2126-166">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="c2126-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="c2126-167">如果沒有指定，則預設為 AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="c2126-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="c2126-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c2126-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="c2126-169">指定 HDInsight 群集將使用之預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c2126-170">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c2126-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="c2126-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="c2126-172">指定在 Data Lake Store 帳戶中，HDInsight 群集將用來做為預設 filesystem 的路徑-前置詞。</span><span class="sxs-lookup"><span data-stu-id="c2126-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="c2126-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="c2126-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="c2126-174">指定群集中輔助角色節點角色的磁片數。</span><span class="sxs-lookup"><span data-stu-id="c2126-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="c2126-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2126-175">-EdgeNodeSize</span></span>
<span data-ttu-id="c2126-176">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c2126-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c2126-177">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c2126-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c2126-178">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="c2126-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c2126-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c2126-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="c2126-180">取得或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="c2126-180">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="c2126-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="c2126-181">-EncryptionAtHost</span></span>
<span data-ttu-id="c2126-182">取得或設定標誌，以指出是否要在主機上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c2126-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="c2126-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="c2126-183">-EncryptionInTransit</span></span>
<span data-ttu-id="c2126-184">取得或設定標誌，以指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c2126-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="c2126-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="c2126-185">-EncryptionKeyName</span></span>
<span data-ttu-id="c2126-186">取得或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="c2126-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c2126-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="c2126-188">取得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="c2126-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="c2126-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="c2126-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="c2126-190">取得或設定加密 vault uri。</span><span class="sxs-lookup"><span data-stu-id="c2126-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="c2126-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2126-191">-HeadNodeSize</span></span>
<span data-ttu-id="c2126-192">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c2126-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c2126-193">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c2126-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c2126-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="c2126-194">-HiveMetastore</span></span>
<span data-ttu-id="c2126-195">指定要儲存 Hive 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c2126-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="c2126-196">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c2126-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c2126-197">-HttpCredential</span></span>
<span data-ttu-id="c2126-198">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="c2126-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="c2126-199">-位置</span><span class="sxs-lookup"><span data-stu-id="c2126-199">-Location</span></span>
<span data-ttu-id="c2126-200">指定群集的位置。</span><span class="sxs-lookup"><span data-stu-id="c2126-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="c2126-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c2126-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="c2126-202">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="c2126-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="c2126-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c2126-203">-ObjectId</span></span>
<span data-ttu-id="c2126-204">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="c2126-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c2126-205">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="c2126-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2126-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c2126-206">-OozieMetastore</span></span>
<span data-ttu-id="c2126-207">指定 SQL 資料庫以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c2126-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="c2126-208">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c2126-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="c2126-209">-OSType</span></span>
<span data-ttu-id="c2126-210">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c2126-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="c2126-211">選項包括： Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="c2126-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="c2126-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="c2126-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="c2126-213">取得或設定公用網路的輸出存取類型。</span><span class="sxs-lookup"><span data-stu-id="c2126-213">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="c2126-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="c2126-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="c2126-215">取得或設定公用網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="c2126-215">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="c2126-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="c2126-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="c2126-217">指定遠端桌面通訊協定的到期日（例如 DateTime 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="c2126-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="c2126-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c2126-218">-RdpCredential</span></span>
<span data-ttu-id="c2126-219">為群集指定遠端桌面 (RDP) 認證。</span><span class="sxs-lookup"><span data-stu-id="c2126-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="c2126-220">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="c2126-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2126-221">-ResourceGroupName</span></span>
<span data-ttu-id="c2126-222">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c2126-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="c2126-223">-ScriptActions</span></span>
<span data-ttu-id="c2126-224">指定在群集建立結束時，要在群集上執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="c2126-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="c2126-225">您也可以使用 [載入 AzHDInsightScriptAction]。</span><span class="sxs-lookup"><span data-stu-id="c2126-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="c2126-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="c2126-226">-SecurityProfile</span></span>
<span data-ttu-id="c2126-227">指定用來建立安全群集的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="c2126-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="c2126-228">您也可以使用 Add-AzHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2126-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="c2126-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="c2126-229">-SshCredential</span></span>
<span data-ttu-id="c2126-230">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="c2126-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="c2126-231">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="c2126-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c2126-232">-SshPublicKey</span></span>
<span data-ttu-id="c2126-233">指定要用於 SSH 連接的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2126-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="c2126-234">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="c2126-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="c2126-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c2126-235">-SubnetName</span></span>
<span data-ttu-id="c2126-236">在已選取的群集虛擬網路中，指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2126-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="c2126-237">-版本</span><span class="sxs-lookup"><span data-stu-id="c2126-237">-Version</span></span>
<span data-ttu-id="c2126-238">指定 HDInsight 群集的 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="c2126-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="c2126-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c2126-239">-VirtualNetworkId</span></span>
<span data-ttu-id="c2126-240">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2126-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="c2126-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2126-241">-WorkerNodeSize</span></span>
<span data-ttu-id="c2126-242">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c2126-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c2126-243">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c2126-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c2126-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2126-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c2126-245">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="c2126-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c2126-246">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c2126-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c2126-247">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="c2126-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c2126-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2126-248">CommonParameters</span></span>
<span data-ttu-id="c2126-249">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2126-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2126-250">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2126-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2126-251">輸入</span><span class="sxs-lookup"><span data-stu-id="c2126-251">INPUTS</span></span>

### <span data-ttu-id="c2126-252">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c2126-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c2126-253">輸出</span><span class="sxs-lookup"><span data-stu-id="c2126-253">OUTPUTS</span></span>

### <span data-ttu-id="c2126-254">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c2126-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c2126-255">筆記</span><span class="sxs-lookup"><span data-stu-id="c2126-255">NOTES</span></span>
<span data-ttu-id="c2126-256">關鍵字： azure，azurerm，arm，資源，管理，管理員，hadoop，hdinsight，hd，洞察力</span><span class="sxs-lookup"><span data-stu-id="c2126-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="c2126-257">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2126-257">RELATED LINKS</span></span>

[<span data-ttu-id="c2126-258">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c2126-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

