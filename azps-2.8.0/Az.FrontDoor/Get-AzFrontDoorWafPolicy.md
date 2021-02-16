---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5cc2a2e480044aa00c51a18dd116d33bd4c2f72a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398456"
---
# <span data-ttu-id="1da93-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="1da93-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="1da93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1da93-102">SYNOPSIS</span></span>
<span data-ttu-id="1da93-103">取得 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="1da93-103">Get WAF policy</span></span>

## <span data-ttu-id="1da93-104">語法</span><span class="sxs-lookup"><span data-stu-id="1da93-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1da93-105">描述</span><span class="sxs-lookup"><span data-stu-id="1da93-105">DESCRIPTION</span></span>
<span data-ttu-id="1da93-106">**Get-AzFrontDoorWafPolicy** CmdletGet 會取得目前訂閱下資源群組中的 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="1da93-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="1da93-107">例子</span><span class="sxs-lookup"><span data-stu-id="1da93-107">EXAMPLES</span></span>

### <span data-ttu-id="1da93-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1da93-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="1da93-109">在 $policyName 中取得稱為 $resourceGroupName 的 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da93-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="1da93-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="1da93-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="1da93-111">取得所有 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da93-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="1da93-112">參數</span><span class="sxs-lookup"><span data-stu-id="1da93-112">PARAMETERS</span></span>

### <span data-ttu-id="1da93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da93-113">-DefaultProfile</span></span>
<span data-ttu-id="1da93-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1da93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1da93-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1da93-115">-Name</span></span>
<span data-ttu-id="1da93-116">FireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="1da93-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="1da93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da93-117">-ResourceGroupName</span></span>
<span data-ttu-id="1da93-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1da93-118">The resource group name.</span></span>

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

### <span data-ttu-id="1da93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da93-119">CommonParameters</span></span>
<span data-ttu-id="1da93-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1da93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da93-121">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1da93-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da93-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1da93-122">INPUTS</span></span>

### <span data-ttu-id="1da93-123">沒有</span><span class="sxs-lookup"><span data-stu-id="1da93-123">None</span></span>

## <span data-ttu-id="1da93-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1da93-124">OUTPUTS</span></span>

### <span data-ttu-id="1da93-125">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1da93-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="1da93-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1da93-126">NOTES</span></span>

## <span data-ttu-id="1da93-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1da93-127">RELATED LINKS</span></span>

<span data-ttu-id="1da93-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1da93-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
