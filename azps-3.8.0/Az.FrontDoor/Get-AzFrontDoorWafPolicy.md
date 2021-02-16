---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404015"
---
# <span data-ttu-id="b3f46-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="b3f46-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="b3f46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3f46-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f46-103">取得 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="b3f46-103">Get WAF policy</span></span>

## <span data-ttu-id="b3f46-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3f46-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3f46-105">描述</span><span class="sxs-lookup"><span data-stu-id="b3f46-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f46-106">**Get-AzFrontDoorWafPolicy** CmdletGet 會取得目前訂閱下資源群組中的 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="b3f46-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="b3f46-107">例子</span><span class="sxs-lookup"><span data-stu-id="b3f46-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f46-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3f46-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="b3f46-109">在 $policyName 中取得稱為 $resourceGroupName 的 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f46-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="b3f46-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="b3f46-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="b3f46-111">取得所有 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f46-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="b3f46-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3f46-112">PARAMETERS</span></span>

### <span data-ttu-id="b3f46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f46-113">-DefaultProfile</span></span>
<span data-ttu-id="b3f46-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3f46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f46-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3f46-115">-Name</span></span>
<span data-ttu-id="b3f46-116">FireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f46-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3f46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f46-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3f46-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3f46-118">The resource group name.</span></span>

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

### <span data-ttu-id="b3f46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f46-119">CommonParameters</span></span>
<span data-ttu-id="b3f46-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3f46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f46-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3f46-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f46-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b3f46-122">INPUTS</span></span>

### <span data-ttu-id="b3f46-123">沒有</span><span class="sxs-lookup"><span data-stu-id="b3f46-123">None</span></span>

## <span data-ttu-id="b3f46-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b3f46-124">OUTPUTS</span></span>

### <span data-ttu-id="b3f46-125">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b3f46-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="b3f46-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b3f46-126">NOTES</span></span>

## <span data-ttu-id="b3f46-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3f46-127">RELATED LINKS</span></span>

<span data-ttu-id="b3f46-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b3f46-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
