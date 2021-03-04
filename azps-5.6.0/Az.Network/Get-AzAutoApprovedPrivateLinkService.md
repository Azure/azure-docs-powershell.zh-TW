---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912742"
---
# <span data-ttu-id="cd921-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd921-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="cd921-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd921-102">SYNOPSIS</span></span>
<span data-ttu-id="cd921-103">獲得私人連結服務識別碼的陣列，可連結至具有自動核准的私人結束點。</span><span class="sxs-lookup"><span data-stu-id="cd921-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="cd921-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd921-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd921-105">描述</span><span class="sxs-lookup"><span data-stu-id="cd921-105">DESCRIPTION</span></span>
<span data-ttu-id="cd921-106">**Get-AzAutoApprovedPrivateLinkService** 會取得一系列私人連結服務識別碼，可連結至私人結束點，並自動核准。</span><span class="sxs-lookup"><span data-stu-id="cd921-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="cd921-107">例子</span><span class="sxs-lookup"><span data-stu-id="cd921-107">EXAMPLES</span></span>

### <span data-ttu-id="cd921-108">例子</span><span class="sxs-lookup"><span data-stu-id="cd921-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="cd921-109">此範例會傳回私人連結服務識別碼的陣列，可連結至具有自動核准的私人終點。</span><span class="sxs-lookup"><span data-stu-id="cd921-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="cd921-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd921-110">PARAMETERS</span></span>

### <span data-ttu-id="cd921-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd921-111">-DefaultProfile</span></span>
<span data-ttu-id="cd921-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd921-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd921-113">-位置</span><span class="sxs-lookup"><span data-stu-id="cd921-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd921-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd921-114">-ResourceGroupName</span></span>
<span data-ttu-id="cd921-115">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd921-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cd921-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd921-116">CommonParameters</span></span>
<span data-ttu-id="cd921-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd921-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd921-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd921-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd921-119">輸入</span><span class="sxs-lookup"><span data-stu-id="cd921-119">INPUTS</span></span>

### <span data-ttu-id="cd921-120">沒有</span><span class="sxs-lookup"><span data-stu-id="cd921-120">None</span></span>

## <span data-ttu-id="cd921-121">輸出</span><span class="sxs-lookup"><span data-stu-id="cd921-121">OUTPUTS</span></span>

### <span data-ttu-id="cd921-122">Microsoft.Azure.Commands.Network.models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd921-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="cd921-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cd921-123">NOTES</span></span>

## <span data-ttu-id="cd921-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd921-124">RELATED LINKS</span></span>
