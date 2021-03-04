---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 47e40395d9422610bcf6fbd341141ba6e9eb3a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911665"
---
# <span data-ttu-id="65275-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="65275-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="65275-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65275-102">SYNOPSIS</span></span>
<span data-ttu-id="65275-103">新增 Azure 儲存體金鑰至組組物件。</span><span class="sxs-lookup"><span data-stu-id="65275-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="65275-104">語法</span><span class="sxs-lookup"><span data-stu-id="65275-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65275-105">描述</span><span class="sxs-lookup"><span data-stu-id="65275-105">DESCRIPTION</span></span>
<span data-ttu-id="65275-106">**Add-AzHDInsightStorage Cmdlet** 會將 Azure 儲存體帳戶專案新增到由 New-AzHDInsightClusterConfig Cmdlet 所建立之 Azure HDInsight 組New-AzHDInsightClusterConfig物件。</span><span class="sxs-lookup"><span data-stu-id="65275-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="65275-107">例子</span><span class="sxs-lookup"><span data-stu-id="65275-107">EXAMPLES</span></span>

### <span data-ttu-id="65275-108">範例 1：新增 Azure 儲存鍵至組組物件</span><span class="sxs-lookup"><span data-stu-id="65275-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

<span data-ttu-id="65275-109">此命令會將 Blob 儲存帳戶專案新增到名為 your-hadoop-001 的 HDInsight 設定檔。</span><span class="sxs-lookup"><span data-stu-id="65275-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="65275-110">參數</span><span class="sxs-lookup"><span data-stu-id="65275-110">PARAMETERS</span></span>

### <span data-ttu-id="65275-111">-Config</span><span class="sxs-lookup"><span data-stu-id="65275-111">-Config</span></span>
<span data-ttu-id="65275-112">指定此 Cmdlet 修改的 HDInsight 集區組物件。</span><span class="sxs-lookup"><span data-stu-id="65275-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="65275-113">此物件是由 **New-AzHDInsightClusterConfig** Cmdlet 所建立。</span><span class="sxs-lookup"><span data-stu-id="65275-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="65275-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65275-114">-DefaultProfile</span></span>
<span data-ttu-id="65275-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="65275-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65275-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="65275-116">-StorageAccountKey</span></span>
<span data-ttu-id="65275-117">指定要新增到新組集中的儲存空間帳戶的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="65275-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="65275-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65275-118">-StorageAccountName</span></span>
<span data-ttu-id="65275-119">指定要新增到該組集中的儲存空間帳戶的儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="65275-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="65275-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65275-120">CommonParameters</span></span>
<span data-ttu-id="65275-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65275-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65275-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65275-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65275-123">輸入</span><span class="sxs-lookup"><span data-stu-id="65275-123">INPUTS</span></span>

### <span data-ttu-id="65275-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="65275-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="65275-125">輸出</span><span class="sxs-lookup"><span data-stu-id="65275-125">OUTPUTS</span></span>

### <span data-ttu-id="65275-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="65275-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="65275-127">筆記</span><span class="sxs-lookup"><span data-stu-id="65275-127">NOTES</span></span>

## <span data-ttu-id="65275-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="65275-128">RELATED LINKS</span></span>

[<span data-ttu-id="65275-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="65275-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


