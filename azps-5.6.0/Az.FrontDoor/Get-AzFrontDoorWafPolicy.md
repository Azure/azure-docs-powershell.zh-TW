---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 83f2c49eb696ac4e3fef0f411b79af24ae95f56c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902594"
---
# <span data-ttu-id="9369a-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="9369a-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="9369a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9369a-102">SYNOPSIS</span></span>
<span data-ttu-id="9369a-103">取得 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="9369a-103">Get WAF policy</span></span>

## <span data-ttu-id="9369a-104">語法</span><span class="sxs-lookup"><span data-stu-id="9369a-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9369a-105">描述</span><span class="sxs-lookup"><span data-stu-id="9369a-105">DESCRIPTION</span></span>
<span data-ttu-id="9369a-106">**Get-AzFrontDoorWafPolicy** CmdletGet 會取得目前訂閱下資源群組中的 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="9369a-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="9369a-107">例子</span><span class="sxs-lookup"><span data-stu-id="9369a-107">EXAMPLES</span></span>

### <span data-ttu-id="9369a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9369a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="9369a-109">在 $policyName 中取得稱為 $resourceGroupName 的 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9369a-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="9369a-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="9369a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="9369a-111">取得所有 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9369a-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="9369a-112">參數</span><span class="sxs-lookup"><span data-stu-id="9369a-112">PARAMETERS</span></span>

### <span data-ttu-id="9369a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9369a-113">-DefaultProfile</span></span>
<span data-ttu-id="9369a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9369a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9369a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9369a-115">-Name</span></span>
<span data-ttu-id="9369a-116">FireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="9369a-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="9369a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9369a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9369a-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9369a-118">The resource group name.</span></span>

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

### <span data-ttu-id="9369a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9369a-119">CommonParameters</span></span>
<span data-ttu-id="9369a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9369a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9369a-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9369a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9369a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9369a-122">INPUTS</span></span>

### <span data-ttu-id="9369a-123">沒有</span><span class="sxs-lookup"><span data-stu-id="9369a-123">None</span></span>

## <span data-ttu-id="9369a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9369a-124">OUTPUTS</span></span>

### <span data-ttu-id="9369a-125">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9369a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="9369a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9369a-126">NOTES</span></span>

## <span data-ttu-id="9369a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9369a-127">RELATED LINKS</span></span>

<span data-ttu-id="9369a-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9369a-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
