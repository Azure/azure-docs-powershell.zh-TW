---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901850"
---
# <span data-ttu-id="c095f-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="c095f-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="c095f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c095f-102">SYNOPSIS</span></span>
<span data-ttu-id="c095f-103">**Test-AzPrivateLinkServiceVisibility** 會檢查目前使用的私人連結服務是否可見。</span><span class="sxs-lookup"><span data-stu-id="c095f-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="c095f-104">語法</span><span class="sxs-lookup"><span data-stu-id="c095f-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c095f-105">描述</span><span class="sxs-lookup"><span data-stu-id="c095f-105">DESCRIPTION</span></span>
<span data-ttu-id="c095f-106">檢查私人連結服務是否可于目前使用中顯示。</span><span class="sxs-lookup"><span data-stu-id="c095f-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="c095f-107">例子</span><span class="sxs-lookup"><span data-stu-id="c095f-107">EXAMPLES</span></span>

### <span data-ttu-id="c095f-108">範例 1：檢查contoso.cloudapp.azure.com是否可用。</span><span class="sxs-lookup"><span data-stu-id="c095f-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="c095f-109">參數</span><span class="sxs-lookup"><span data-stu-id="c095f-109">PARAMETERS</span></span>

### <span data-ttu-id="c095f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c095f-110">-DefaultProfile</span></span>
<span data-ttu-id="c095f-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c095f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c095f-112">-位置</span><span class="sxs-lookup"><span data-stu-id="c095f-112">-Location</span></span>
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

### <span data-ttu-id="c095f-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="c095f-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c095f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c095f-114">-ResourceGroupName</span></span>
<span data-ttu-id="c095f-115">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c095f-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c095f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c095f-116">CommonParameters</span></span>
<span data-ttu-id="c095f-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c095f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c095f-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c095f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c095f-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c095f-119">INPUTS</span></span>

### <span data-ttu-id="c095f-120">沒有</span><span class="sxs-lookup"><span data-stu-id="c095f-120">None</span></span>

## <span data-ttu-id="c095f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c095f-121">OUTPUTS</span></span>

### <span data-ttu-id="c095f-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c095f-122">System.Boolean</span></span>

## <span data-ttu-id="c095f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c095f-123">NOTES</span></span>

## <span data-ttu-id="c095f-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c095f-124">RELATED LINKS</span></span>
