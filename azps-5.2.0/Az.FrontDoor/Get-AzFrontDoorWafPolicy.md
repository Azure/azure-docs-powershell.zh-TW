---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280231"
---
# <span data-ttu-id="5e0d1-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="5e0d1-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="5e0d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0d1-103">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="5e0d1-103">Get WAF policy</span></span>

## <span data-ttu-id="5e0d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e0d1-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e0d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e0d1-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0d1-106">**AzFrontDoorWafPolicy** CmdletGet 會在目前訂閱底下的資源群組中取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="5e0d1-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="5e0d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e0d1-107">EXAMPLES</span></span>

### <span data-ttu-id="5e0d1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5e0d1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="5e0d1-109">在 $resourceGroupName 中取得稱為 $policyName 的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="5e0d1-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="5e0d1-110">範例2</span><span class="sxs-lookup"><span data-stu-id="5e0d1-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="5e0d1-111">取得 $resourceGroupName 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="5e0d1-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="5e0d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="5e0d1-112">PARAMETERS</span></span>

### <span data-ttu-id="5e0d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0d1-113">-DefaultProfile</span></span>
<span data-ttu-id="5e0d1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e0d1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e0d1-115">-Name</span></span>
<span data-ttu-id="5e0d1-116">FireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="5e0d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e0d1-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-118">The resource group name.</span></span>

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

### <span data-ttu-id="5e0d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0d1-119">CommonParameters</span></span>
<span data-ttu-id="5e0d1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0d1-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0d1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5e0d1-122">INPUTS</span></span>

### <span data-ttu-id="5e0d1-123">所有</span><span class="sxs-lookup"><span data-stu-id="5e0d1-123">None</span></span>

## <span data-ttu-id="5e0d1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5e0d1-124">OUTPUTS</span></span>

### <span data-ttu-id="5e0d1-125">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="5e0d1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5e0d1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5e0d1-126">NOTES</span></span>

## <span data-ttu-id="5e0d1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e0d1-127">RELATED LINKS</span></span>

<span data-ttu-id="5e0d1-128">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[更新-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[移除-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="5e0d1-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
