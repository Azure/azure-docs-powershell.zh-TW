---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624376"
---
# <span data-ttu-id="a029b-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a029b-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="a029b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a029b-102">SYNOPSIS</span></span>
<span data-ttu-id="a029b-103">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="a029b-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a029b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a029b-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a029b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a029b-105">DESCRIPTION</span></span>
<span data-ttu-id="a029b-106">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="a029b-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="a029b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a029b-107">EXAMPLES</span></span>

### <span data-ttu-id="a029b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a029b-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="a029b-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="a029b-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="a029b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a029b-110">PARAMETERS</span></span>

### <span data-ttu-id="a029b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a029b-111">-DefaultProfile</span></span>
<span data-ttu-id="a029b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a029b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a029b-113">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a029b-113">-Priority</span></span>
<span data-ttu-id="a029b-114">描述規則的優先順序</span><span class="sxs-lookup"><span data-stu-id="a029b-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a029b-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a029b-115">-RuleGroupOverride</span></span>
<span data-ttu-id="a029b-116">Azure managed 提供者覆蓋設定的清單</span><span class="sxs-lookup"><span data-stu-id="a029b-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a029b-117">-版本</span><span class="sxs-lookup"><span data-stu-id="a029b-117">-Version</span></span>
<span data-ttu-id="a029b-118">版本的規則集</span><span class="sxs-lookup"><span data-stu-id="a029b-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="a029b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a029b-119">CommonParameters</span></span>
<span data-ttu-id="a029b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a029b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a029b-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a029b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a029b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a029b-122">INPUTS</span></span>

### <span data-ttu-id="a029b-123">所有</span><span class="sxs-lookup"><span data-stu-id="a029b-123">None</span></span>

## <span data-ttu-id="a029b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a029b-124">OUTPUTS</span></span>

### <span data-ttu-id="a029b-125">PSAzureManagedRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="a029b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="a029b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a029b-126">NOTES</span></span>

## <span data-ttu-id="a029b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a029b-127">RELATED LINKS</span></span>

<span data-ttu-id="a029b-128">[新-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
[新-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="a029b-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
