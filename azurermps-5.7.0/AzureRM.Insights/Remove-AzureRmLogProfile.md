---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447796"
---
# <span data-ttu-id="942bc-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="942bc-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="942bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="942bc-102">SYNOPSIS</span></span>
<span data-ttu-id="942bc-103">移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="942bc-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="942bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="942bc-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="942bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="942bc-105">DESCRIPTION</span></span>
<span data-ttu-id="942bc-106">**AzureRmLogProfile** Cmdlet 會移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="942bc-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="942bc-107">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="942bc-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="942bc-108">示例</span><span class="sxs-lookup"><span data-stu-id="942bc-108">EXAMPLES</span></span>

## <span data-ttu-id="942bc-109">參數</span><span class="sxs-lookup"><span data-stu-id="942bc-109">PARAMETERS</span></span>

### <span data-ttu-id="942bc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942bc-110">-DefaultProfile</span></span>
<span data-ttu-id="942bc-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="942bc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="942bc-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="942bc-112">-Name</span></span>
<span data-ttu-id="942bc-113">指定要移除的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="942bc-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="942bc-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="942bc-114">-PassThru</span></span>
<span data-ttu-id="942bc-115">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="942bc-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942bc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942bc-116">CommonParameters</span></span>
<span data-ttu-id="942bc-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="942bc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942bc-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="942bc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942bc-119">輸入</span><span class="sxs-lookup"><span data-stu-id="942bc-119">INPUTS</span></span>

### <span data-ttu-id="942bc-120">所有</span><span class="sxs-lookup"><span data-stu-id="942bc-120">None</span></span>
<span data-ttu-id="942bc-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="942bc-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="942bc-122">輸出</span><span class="sxs-lookup"><span data-stu-id="942bc-122">OUTPUTS</span></span>

### <span data-ttu-id="942bc-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="942bc-123">AzureOperationResponse</span></span>

## <span data-ttu-id="942bc-124">筆記</span><span class="sxs-lookup"><span data-stu-id="942bc-124">NOTES</span></span>

## <span data-ttu-id="942bc-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="942bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="942bc-126">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="942bc-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="942bc-127">AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="942bc-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


