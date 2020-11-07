---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 43418937c379ba1ac93b5a2c733028e31eef7318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624306"
---
# <span data-ttu-id="e8153-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e8153-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="e8153-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8153-102">SYNOPSIS</span></span>
<span data-ttu-id="e8153-103">在群集設定物件中設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="e8153-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8153-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8153-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8153-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8153-105">DESCRIPTION</span></span>
<span data-ttu-id="e8153-106">**AzureRmHDInsightDefaultStorage** Cmdlet 會在由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 Azure HDInsight 群集設定物件中，設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="e8153-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e8153-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8153-107">EXAMPLES</span></span>

### <span data-ttu-id="e8153-108">範例1：設定 [群集] 設定物件的預設儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="e8153-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="e8153-109">這個命令會設定群集設定物件的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e8153-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="e8153-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8153-110">PARAMETERS</span></span>

### <span data-ttu-id="e8153-111">-Config</span><span class="sxs-lookup"><span data-stu-id="e8153-111">-Config</span></span>
<span data-ttu-id="e8153-112">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="e8153-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e8153-113">這個物件是由 **新的-AzureRmHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="e8153-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8153-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8153-114">-DefaultProfile</span></span>
<span data-ttu-id="e8153-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e8153-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8153-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e8153-116">-StorageAccountKey</span></span>
<span data-ttu-id="e8153-117">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8153-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8153-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8153-118">-StorageAccountName</span></span>
<span data-ttu-id="e8153-119">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8153-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8153-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e8153-120">-StorageAccountType</span></span>
<span data-ttu-id="e8153-121">取得或設定預設儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="e8153-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="e8153-122">預設為 AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e8153-122">Defaults to AzureStorage</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8153-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8153-123">CommonParameters</span></span>
<span data-ttu-id="e8153-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8153-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8153-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8153-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8153-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e8153-126">INPUTS</span></span>

### <span data-ttu-id="e8153-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e8153-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="e8153-128">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e8153-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="e8153-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e8153-129">OUTPUTS</span></span>

### <span data-ttu-id="e8153-130">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e8153-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e8153-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e8153-131">NOTES</span></span>

## <span data-ttu-id="e8153-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8153-132">RELATED LINKS</span></span>
