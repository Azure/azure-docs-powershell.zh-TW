---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 29ff6159501bccd73947e25a65ec765a49b8859c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799953"
---
# <span data-ttu-id="b6551-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b6551-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="b6551-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6551-102">SYNOPSIS</span></span>
<span data-ttu-id="b6551-103">取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6551-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6551-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6551-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6551-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6551-105">DESCRIPTION</span></span>
<span data-ttu-id="b6551-106">**AzureRmLogProfile** Cmdlet 會取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6551-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="b6551-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6551-107">EXAMPLES</span></span>

## <span data-ttu-id="b6551-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6551-108">PARAMETERS</span></span>

### <span data-ttu-id="b6551-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6551-109">-DefaultProfile</span></span>
<span data-ttu-id="b6551-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b6551-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6551-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6551-111">-Name</span></span>
<span data-ttu-id="b6551-112">指定要取得的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b6551-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6551-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6551-113">CommonParameters</span></span>
<span data-ttu-id="b6551-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6551-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6551-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6551-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6551-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b6551-116">INPUTS</span></span>

### <span data-ttu-id="b6551-117">System.object</span><span class="sxs-lookup"><span data-stu-id="b6551-117">System.String</span></span>

## <span data-ttu-id="b6551-118">輸出</span><span class="sxs-lookup"><span data-stu-id="b6551-118">OUTPUTS</span></span>

### <span data-ttu-id="b6551-119">PSLogProfileCollection 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="b6551-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="b6551-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b6551-120">NOTES</span></span>

## <span data-ttu-id="b6551-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6551-121">RELATED LINKS</span></span>

[<span data-ttu-id="b6551-122">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b6551-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="b6551-123">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b6551-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


