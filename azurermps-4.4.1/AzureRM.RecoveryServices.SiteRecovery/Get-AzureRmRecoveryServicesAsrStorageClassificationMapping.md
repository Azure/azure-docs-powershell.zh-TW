---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625105"
---
# <span data-ttu-id="297a4-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="297a4-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="297a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="297a4-102">SYNOPSIS</span></span>
<span data-ttu-id="297a4-103">取得 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="297a4-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="297a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="297a4-104">SYNTAX</span></span>

### <span data-ttu-id="297a4-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="297a4-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="297a4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="297a4-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="297a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="297a4-107">DESCRIPTION</span></span>
<span data-ttu-id="297a4-108">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會取得 ASR 儲存分類對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="297a4-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="297a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="297a4-109">EXAMPLES</span></span>

### <span data-ttu-id="297a4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="297a4-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="297a4-111">列出與指定的儲存分類相關的所有儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="297a4-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="297a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="297a4-112">PARAMETERS</span></span>

### <span data-ttu-id="297a4-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="297a4-113">-Name</span></span>
<span data-ttu-id="297a4-114">指定要取得之儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="297a4-114">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="297a4-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="297a4-115">-StorageClassification</span></span>
<span data-ttu-id="297a4-116">指定 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="297a4-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="297a4-117">這個 Cmdlet 會取得與指定的儲存分類相對應的 ASR 儲存分類對應</span><span class="sxs-lookup"><span data-stu-id="297a4-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="297a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297a4-118">CommonParameters</span></span>
<span data-ttu-id="297a4-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="297a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297a4-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="297a4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297a4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="297a4-121">INPUTS</span></span>

### <span data-ttu-id="297a4-122">所有</span><span class="sxs-lookup"><span data-stu-id="297a4-122">None</span></span>

## <span data-ttu-id="297a4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="297a4-123">OUTPUTS</span></span>

### <span data-ttu-id="297a4-124">System.object. IEnumerable "1 [ASRStorageClassificationMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="297a4-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="297a4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="297a4-125">NOTES</span></span>

## <span data-ttu-id="297a4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="297a4-126">RELATED LINKS</span></span>

[<span data-ttu-id="297a4-127">新-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="297a4-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="297a4-128">移除-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="297a4-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
