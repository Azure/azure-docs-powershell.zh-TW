---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143119"
---
# <span data-ttu-id="03cfc-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="03cfc-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="03cfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="03cfc-103">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="03cfc-103">Get WAF policy</span></span>

## <span data-ttu-id="03cfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="03cfc-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03cfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="03cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="03cfc-106">**AzFrontDoorWafPolicy** CmdletGet 會在目前訂閱底下的資源群組中取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="03cfc-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="03cfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="03cfc-107">EXAMPLES</span></span>

### <span data-ttu-id="03cfc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="03cfc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="03cfc-109">在 $resourceGroupName 中取得稱為 $policyName 的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="03cfc-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="03cfc-110">範例2</span><span class="sxs-lookup"><span data-stu-id="03cfc-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="03cfc-111">取得 $resourceGroupName 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="03cfc-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="03cfc-112">參數</span><span class="sxs-lookup"><span data-stu-id="03cfc-112">PARAMETERS</span></span>

### <span data-ttu-id="03cfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03cfc-113">-DefaultProfile</span></span>
<span data-ttu-id="03cfc-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03cfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03cfc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="03cfc-115">-Name</span></span>
<span data-ttu-id="03cfc-116">FireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="03cfc-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="03cfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03cfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="03cfc-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03cfc-118">The resource group name.</span></span>

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

### <span data-ttu-id="03cfc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03cfc-119">CommonParameters</span></span>
<span data-ttu-id="03cfc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03cfc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03cfc-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="03cfc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03cfc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="03cfc-122">INPUTS</span></span>

### <span data-ttu-id="03cfc-123">所有</span><span class="sxs-lookup"><span data-stu-id="03cfc-123">None</span></span>

## <span data-ttu-id="03cfc-124">輸出</span><span class="sxs-lookup"><span data-stu-id="03cfc-124">OUTPUTS</span></span>

### <span data-ttu-id="03cfc-125">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="03cfc-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="03cfc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="03cfc-126">NOTES</span></span>

## <span data-ttu-id="03cfc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="03cfc-127">RELATED LINKS</span></span>

<span data-ttu-id="03cfc-128">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[更新-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[移除-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="03cfc-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
