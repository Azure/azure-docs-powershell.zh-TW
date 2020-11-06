---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456072"
---
# <span data-ttu-id="0d560-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0d560-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="0d560-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d560-102">SYNOPSIS</span></span>
<span data-ttu-id="0d560-103">取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d560-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d560-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d560-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d560-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d560-105">DESCRIPTION</span></span>
<span data-ttu-id="0d560-106">**AzureRmLogProfile** Cmdlet 會取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d560-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="0d560-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d560-107">EXAMPLES</span></span>

## <span data-ttu-id="0d560-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d560-108">PARAMETERS</span></span>

### <span data-ttu-id="0d560-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d560-109">-DefaultProfile</span></span>
<span data-ttu-id="0d560-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0d560-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d560-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d560-111">-Name</span></span>
<span data-ttu-id="0d560-112">指定要取得的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="0d560-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="0d560-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d560-113">CommonParameters</span></span>
<span data-ttu-id="0d560-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d560-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d560-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d560-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d560-116">輸入</span><span class="sxs-lookup"><span data-stu-id="0d560-116">INPUTS</span></span>

### <span data-ttu-id="0d560-117">System.object</span><span class="sxs-lookup"><span data-stu-id="0d560-117">System.String</span></span>

## <span data-ttu-id="0d560-118">輸出</span><span class="sxs-lookup"><span data-stu-id="0d560-118">OUTPUTS</span></span>

### <span data-ttu-id="0d560-119">PSLogProfileCollection 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="0d560-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="0d560-120">筆記</span><span class="sxs-lookup"><span data-stu-id="0d560-120">NOTES</span></span>

## <span data-ttu-id="0d560-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d560-121">RELATED LINKS</span></span>

[<span data-ttu-id="0d560-122">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0d560-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="0d560-123">移除-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0d560-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


