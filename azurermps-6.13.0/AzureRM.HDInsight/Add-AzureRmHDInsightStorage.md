---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: 1d81b5c528739fb012f90e6e112422c4e828c1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449163"
---
# <span data-ttu-id="9af82-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="9af82-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="9af82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9af82-102">SYNOPSIS</span></span>
<span data-ttu-id="9af82-103">將 Azure 儲存空間金鑰新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9af82-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af82-104">句法</span><span class="sxs-lookup"><span data-stu-id="9af82-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af82-105">說明</span><span class="sxs-lookup"><span data-stu-id="9af82-105">DESCRIPTION</span></span>
<span data-ttu-id="9af82-106">**AzureRmHDInsightStorage** Cmdlet 會將 Azure 儲存空間帳戶專案新增至由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 azure HDInsight configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="9af82-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9af82-107">示例</span><span class="sxs-lookup"><span data-stu-id="9af82-107">EXAMPLES</span></span>

### <span data-ttu-id="9af82-108">範例1：新增 Azure 存儲金鑰至 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="9af82-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="9af82-109">這個命令會將 [blob 儲存空間] 帳戶專案新增到名為 [hadoop-001] 的 HDInsight 配置中。</span><span class="sxs-lookup"><span data-stu-id="9af82-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="9af82-110">參數</span><span class="sxs-lookup"><span data-stu-id="9af82-110">PARAMETERS</span></span>

### <span data-ttu-id="9af82-111">-Config</span><span class="sxs-lookup"><span data-stu-id="9af82-111">-Config</span></span>
<span data-ttu-id="9af82-112">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="9af82-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="9af82-113">這個物件是由 **新的-AzureRmHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="9af82-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="9af82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af82-114">-DefaultProfile</span></span>
<span data-ttu-id="9af82-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9af82-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9af82-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9af82-116">-StorageAccountKey</span></span>
<span data-ttu-id="9af82-117">指定要新增至新群集之儲存空間帳戶的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="9af82-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="9af82-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9af82-118">-StorageAccountName</span></span>
<span data-ttu-id="9af82-119">指定要新增至群集之儲存帳戶的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9af82-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="9af82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af82-120">CommonParameters</span></span>
<span data-ttu-id="9af82-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9af82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af82-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9af82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af82-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9af82-123">INPUTS</span></span>

### <span data-ttu-id="9af82-124">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="9af82-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="9af82-125">參數： Config (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9af82-125">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="9af82-126">輸出</span><span class="sxs-lookup"><span data-stu-id="9af82-126">OUTPUTS</span></span>

### <span data-ttu-id="9af82-127">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="9af82-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9af82-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9af82-128">NOTES</span></span>

## <span data-ttu-id="9af82-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9af82-129">RELATED LINKS</span></span>

[<span data-ttu-id="9af82-130">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9af82-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


