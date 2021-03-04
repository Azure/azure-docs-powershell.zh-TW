---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 9873ba2e4fa4f54c4aa77822af076bb5426ac198
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914833"
---
# <span data-ttu-id="021a3-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="021a3-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="021a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="021a3-102">SYNOPSIS</span></span>
<span data-ttu-id="021a3-103">設定組組設定物件中的預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="021a3-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="021a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="021a3-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="021a3-105">描述</span><span class="sxs-lookup"><span data-stu-id="021a3-105">DESCRIPTION</span></span>
<span data-ttu-id="021a3-106">**Set-AzHDInsightDefaultStorage Cmdlet** 會設定由 New-AzHDInsightClusterConfig Cmdlet 所建立之 Azure HDInsight New-AzHDInsightClusterConfig組組設定的預設儲存帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="021a3-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="021a3-107">例子</span><span class="sxs-lookup"><span data-stu-id="021a3-107">EXAMPLES</span></span>

### <span data-ttu-id="021a3-108">範例 1：設定組組設定物件的預設儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="021a3-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="021a3-109">此命令會設定組組設定物件的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="021a3-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="021a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="021a3-110">PARAMETERS</span></span>

### <span data-ttu-id="021a3-111">-Config</span><span class="sxs-lookup"><span data-stu-id="021a3-111">-Config</span></span>
<span data-ttu-id="021a3-112">指定此 Cmdlet 修改的 HDInsight 集區組物件。</span><span class="sxs-lookup"><span data-stu-id="021a3-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="021a3-113">此物件是由 **New-AzHDInsightClusterConfig** Cmdlet 所建立。</span><span class="sxs-lookup"><span data-stu-id="021a3-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="021a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021a3-114">-DefaultProfile</span></span>
<span data-ttu-id="021a3-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="021a3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="021a3-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="021a3-116">-StorageAccountKey</span></span>
<span data-ttu-id="021a3-117">指定 HDInsight 組會使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="021a3-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021a3-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="021a3-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="021a3-119">要新增到新集區之儲存空間帳戶的儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="021a3-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="021a3-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="021a3-120">-StorageAccountType</span></span>
<span data-ttu-id="021a3-121">獲取或設定預設儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="021a3-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="021a3-122">AzureStorage 的預設值</span><span class="sxs-lookup"><span data-stu-id="021a3-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="021a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021a3-123">CommonParameters</span></span>
<span data-ttu-id="021a3-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="021a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021a3-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="021a3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021a3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="021a3-126">INPUTS</span></span>

### <span data-ttu-id="021a3-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="021a3-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="021a3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="021a3-128">OUTPUTS</span></span>

### <span data-ttu-id="021a3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="021a3-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="021a3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="021a3-130">NOTES</span></span>

## <span data-ttu-id="021a3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="021a3-131">RELATED LINKS</span></span>
