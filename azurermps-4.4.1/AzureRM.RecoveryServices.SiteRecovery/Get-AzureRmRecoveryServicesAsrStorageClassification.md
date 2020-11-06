---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455635"
---
# <span data-ttu-id="cf50a-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="cf50a-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="cf50a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf50a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf50a-103">取得在復原服務電子倉庫中) ASR 儲存空間分類中發現的可用 (。</span><span class="sxs-lookup"><span data-stu-id="cf50a-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf50a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf50a-104">SYNTAX</span></span>

### <span data-ttu-id="cf50a-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="cf50a-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="cf50a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="cf50a-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="cf50a-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf50a-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="cf50a-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf50a-108">DESCRIPTION</span></span>
<span data-ttu-id="cf50a-109">**AzureRmRecoveryServicesAsrStorageClassification** Cmdlet 會在復原服務電子倉庫中取得已探索之 ASR 儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf50a-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="cf50a-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf50a-110">EXAMPLES</span></span>

### <span data-ttu-id="cf50a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cf50a-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="cf50a-112">列出與指定的 ASR 結構相對應的已探索儲存分類。</span><span class="sxs-lookup"><span data-stu-id="cf50a-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="cf50a-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf50a-113">PARAMETERS</span></span>

### <span data-ttu-id="cf50a-114">-結構</span><span class="sxs-lookup"><span data-stu-id="cf50a-114">-Fabric</span></span>
<span data-ttu-id="cf50a-115">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="cf50a-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="cf50a-116">這個 Cmdlet 會取得與指定的 ASR 結構相對應的已探索儲存空間分類的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf50a-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf50a-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf50a-117">-FriendlyName</span></span>
<span data-ttu-id="cf50a-118">指定要取得的儲存分類物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="cf50a-118">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf50a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf50a-119">-Name</span></span>
<span data-ttu-id="cf50a-120">指定要取得之儲存分類物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf50a-120">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf50a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf50a-121">CommonParameters</span></span>
<span data-ttu-id="cf50a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf50a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf50a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf50a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf50a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cf50a-124">INPUTS</span></span>

### <span data-ttu-id="cf50a-125">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cf50a-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="cf50a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cf50a-126">OUTPUTS</span></span>

### <span data-ttu-id="cf50a-127">System.object. IEnumerable "1 [ASRStorageClassification，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="cf50a-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cf50a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cf50a-128">NOTES</span></span>

## <span data-ttu-id="cf50a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf50a-129">RELATED LINKS</span></span>

