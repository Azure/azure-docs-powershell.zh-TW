---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: b96c8717e20395c57e6c9d5d4520327d97dfa174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448651"
---
# <span data-ttu-id="8167b-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8167b-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="8167b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8167b-102">SYNOPSIS</span></span>
<span data-ttu-id="8167b-103">取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="8167b-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8167b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8167b-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8167b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8167b-105">DESCRIPTION</span></span>
<span data-ttu-id="8167b-106">**AzureRmLogProfile** Cmdlet 會取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="8167b-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="8167b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8167b-107">EXAMPLES</span></span>

## <span data-ttu-id="8167b-108">參數</span><span class="sxs-lookup"><span data-stu-id="8167b-108">PARAMETERS</span></span>

### <span data-ttu-id="8167b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8167b-109">-DefaultProfile</span></span>
<span data-ttu-id="8167b-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8167b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8167b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8167b-111">-Name</span></span>
<span data-ttu-id="8167b-112">指定要取得的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="8167b-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8167b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8167b-113">CommonParameters</span></span>
<span data-ttu-id="8167b-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8167b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8167b-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8167b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8167b-116">輸入</span><span class="sxs-lookup"><span data-stu-id="8167b-116">INPUTS</span></span>

### <span data-ttu-id="8167b-117">所有</span><span class="sxs-lookup"><span data-stu-id="8167b-117">None</span></span>
<span data-ttu-id="8167b-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8167b-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8167b-119">輸出</span><span class="sxs-lookup"><span data-stu-id="8167b-119">OUTPUTS</span></span>

### <span data-ttu-id="8167b-120">PSLogProfileCollection 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="8167b-120">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="8167b-121">筆記</span><span class="sxs-lookup"><span data-stu-id="8167b-121">NOTES</span></span>

## <span data-ttu-id="8167b-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="8167b-122">RELATED LINKS</span></span>

[<span data-ttu-id="8167b-123">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8167b-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="8167b-124">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="8167b-124">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


