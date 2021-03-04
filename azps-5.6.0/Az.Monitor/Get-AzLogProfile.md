---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908925"
---
# <span data-ttu-id="6e65b-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6e65b-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="6e65b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e65b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e65b-103">獲得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="6e65b-103">Gets a log profile.</span></span>

## <span data-ttu-id="6e65b-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e65b-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e65b-105">描述</span><span class="sxs-lookup"><span data-stu-id="6e65b-105">DESCRIPTION</span></span>
<span data-ttu-id="6e65b-106">**Get-AzLogProfile** Cmdlet 會取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="6e65b-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="6e65b-107">例子</span><span class="sxs-lookup"><span data-stu-id="6e65b-107">EXAMPLES</span></span>

## <span data-ttu-id="6e65b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e65b-108">PARAMETERS</span></span>

### <span data-ttu-id="6e65b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e65b-109">-DefaultProfile</span></span>
<span data-ttu-id="6e65b-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6e65b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e65b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e65b-111">-Name</span></span>
<span data-ttu-id="6e65b-112">指定要取得之記錄設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e65b-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="6e65b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e65b-113">CommonParameters</span></span>
<span data-ttu-id="6e65b-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e65b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e65b-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e65b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e65b-116">輸入</span><span class="sxs-lookup"><span data-stu-id="6e65b-116">INPUTS</span></span>

### <span data-ttu-id="6e65b-117">System.String</span><span class="sxs-lookup"><span data-stu-id="6e65b-117">System.String</span></span>

## <span data-ttu-id="6e65b-118">輸出</span><span class="sxs-lookup"><span data-stu-id="6e65b-118">OUTPUTS</span></span>

### <span data-ttu-id="6e65b-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="6e65b-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="6e65b-120">筆記</span><span class="sxs-lookup"><span data-stu-id="6e65b-120">NOTES</span></span>

## <span data-ttu-id="6e65b-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e65b-121">RELATED LINKS</span></span>

[<span data-ttu-id="6e65b-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6e65b-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="6e65b-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6e65b-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


