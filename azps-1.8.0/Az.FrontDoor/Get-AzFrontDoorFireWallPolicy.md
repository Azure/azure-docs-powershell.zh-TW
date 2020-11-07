---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: e8fe8fb59ee56e457c49d959c07db08cad62bb5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787841"
---
# <span data-ttu-id="cdb65-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="cdb65-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="cdb65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdb65-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb65-103">取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="cdb65-103">Get WAF policy</span></span>

## <span data-ttu-id="cdb65-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdb65-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdb65-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdb65-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb65-106">**AzFrontDoorFireWallPolicy** CmdletGet 會在目前訂閱底下的資源群組中取得 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="cdb65-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="cdb65-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdb65-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb65-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cdb65-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="cdb65-109">在 $resourceGroupName 中取得稱為 $policyName 的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="cdb65-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="cdb65-110">範例2</span><span class="sxs-lookup"><span data-stu-id="cdb65-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="cdb65-111">取得 $resourceGroupName 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="cdb65-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="cdb65-112">參數</span><span class="sxs-lookup"><span data-stu-id="cdb65-112">PARAMETERS</span></span>

### <span data-ttu-id="cdb65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb65-113">-DefaultProfile</span></span>
<span data-ttu-id="cdb65-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdb65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb65-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdb65-115">-Name</span></span>
<span data-ttu-id="cdb65-116">FireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="cdb65-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="cdb65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb65-117">-ResourceGroupName</span></span>
<span data-ttu-id="cdb65-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb65-118">The resource group name.</span></span>

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

### <span data-ttu-id="cdb65-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb65-119">CommonParameters</span></span>
<span data-ttu-id="cdb65-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdb65-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb65-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cdb65-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb65-122">輸入</span><span class="sxs-lookup"><span data-stu-id="cdb65-122">INPUTS</span></span>

### <span data-ttu-id="cdb65-123">所有</span><span class="sxs-lookup"><span data-stu-id="cdb65-123">None</span></span>

## <span data-ttu-id="cdb65-124">輸出</span><span class="sxs-lookup"><span data-stu-id="cdb65-124">OUTPUTS</span></span>

### <span data-ttu-id="cdb65-125">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="cdb65-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="cdb65-126">筆記</span><span class="sxs-lookup"><span data-stu-id="cdb65-126">NOTES</span></span>

## <span data-ttu-id="cdb65-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdb65-127">RELATED LINKS</span></span>

<span data-ttu-id="cdb65-128">[新-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
[移除-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="cdb65-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span></span>
