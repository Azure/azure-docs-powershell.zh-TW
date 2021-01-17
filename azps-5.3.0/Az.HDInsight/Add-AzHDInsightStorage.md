---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 6db3c5b5d899f9b7a32e6dbb20c280590bea93c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435068"
---
# <span data-ttu-id="f2b79-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f2b79-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="f2b79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2b79-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b79-103">將 Azure 儲存空間金鑰新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f2b79-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="f2b79-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2b79-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b79-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2b79-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b79-106">**AzHDInsightStorage** Cmdlet 會將 Azure 儲存空間帳戶專案新增至由 New-AzHDInsightClusterConfig Cmdlet 建立的 azure HDInsight configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="f2b79-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f2b79-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2b79-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b79-108">範例1：新增 Azure 存儲金鑰至 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="f2b79-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="f2b79-109">這個命令會將 [blob 儲存空間] 帳戶專案新增到名為 [hadoop-001] 的 HDInsight 配置中。</span><span class="sxs-lookup"><span data-stu-id="f2b79-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="f2b79-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2b79-110">PARAMETERS</span></span>

### <span data-ttu-id="f2b79-111">-Config</span><span class="sxs-lookup"><span data-stu-id="f2b79-111">-Config</span></span>
<span data-ttu-id="f2b79-112">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="f2b79-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f2b79-113">這個物件是由 **新的-AzHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="f2b79-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b79-114">-DefaultProfile</span></span>
<span data-ttu-id="f2b79-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f2b79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2b79-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f2b79-116">-StorageAccountKey</span></span>
<span data-ttu-id="f2b79-117">指定要新增至新群集之儲存空間帳戶的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="f2b79-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="f2b79-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f2b79-118">-StorageAccountName</span></span>
<span data-ttu-id="f2b79-119">指定要新增至群集之儲存帳戶的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f2b79-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="f2b79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b79-120">CommonParameters</span></span>
<span data-ttu-id="f2b79-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2b79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b79-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2b79-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b79-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f2b79-123">INPUTS</span></span>

### <span data-ttu-id="f2b79-124">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f2b79-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f2b79-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f2b79-125">OUTPUTS</span></span>

### <span data-ttu-id="f2b79-126">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f2b79-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f2b79-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f2b79-127">NOTES</span></span>

## <span data-ttu-id="f2b79-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2b79-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2b79-129">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f2b79-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


