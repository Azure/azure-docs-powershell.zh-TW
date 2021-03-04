---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 889e4a0651c9aa3ccbe91227db803958fcb3c7bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910645"
---
# <span data-ttu-id="a5455-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a5455-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="a5455-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5455-102">SYNOPSIS</span></span>
<span data-ttu-id="a5455-103">更新安全性警示狀態。</span><span class="sxs-lookup"><span data-stu-id="a5455-103">Updates a security alert state.</span></span>

## <span data-ttu-id="a5455-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5455-104">SYNTAX</span></span>

### <span data-ttu-id="a5455-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a5455-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5455-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a5455-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5455-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5455-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5455-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="a5455-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5455-109">描述</span><span class="sxs-lookup"><span data-stu-id="a5455-109">DESCRIPTION</span></span>
<span data-ttu-id="a5455-110">設定安全性警示狀態。</span><span class="sxs-lookup"><span data-stu-id="a5455-110">Sets a security alert state.</span></span>

## <span data-ttu-id="a5455-111">例子</span><span class="sxs-lookup"><span data-stu-id="a5455-111">EXAMPLES</span></span>

### <span data-ttu-id="a5455-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5455-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="a5455-113">關閉系統所發出的安全性警訊。</span><span class="sxs-lookup"><span data-stu-id="a5455-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="a5455-114">參數</span><span class="sxs-lookup"><span data-stu-id="a5455-114">PARAMETERS</span></span>

### <span data-ttu-id="a5455-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="a5455-115">-ActionType</span></span>
<span data-ttu-id="a5455-116">動作類型。</span><span class="sxs-lookup"><span data-stu-id="a5455-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5455-117">-DefaultProfile</span></span>
<span data-ttu-id="a5455-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5455-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5455-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5455-119">-InputObject</span></span>
<span data-ttu-id="a5455-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a5455-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-121">-位置</span><span class="sxs-lookup"><span data-stu-id="a5455-121">-Location</span></span>
<span data-ttu-id="a5455-122">位置。</span><span class="sxs-lookup"><span data-stu-id="a5455-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5455-123">-Name</span></span>
<span data-ttu-id="a5455-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a5455-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5455-125">-PassThru</span></span>
<span data-ttu-id="a5455-126">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="a5455-126">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5455-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5455-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a5455-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5455-129">-ResourceId</span></span>
<span data-ttu-id="a5455-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5455-130">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a5455-131">-Confirm</span></span>
<span data-ttu-id="a5455-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5455-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5455-133">-WhatIf</span></span>
<span data-ttu-id="a5455-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5455-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5455-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5455-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5455-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5455-136">CommonParameters</span></span>
<span data-ttu-id="a5455-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5455-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5455-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5455-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5455-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a5455-139">INPUTS</span></span>

### <span data-ttu-id="a5455-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a5455-140">System.String</span></span>

### <span data-ttu-id="a5455-141">Microsoft.Azure.Commands.security.models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a5455-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="a5455-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a5455-142">OUTPUTS</span></span>

### <span data-ttu-id="a5455-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5455-143">System.Boolean</span></span>

## <span data-ttu-id="a5455-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a5455-144">NOTES</span></span>

## <span data-ttu-id="a5455-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5455-145">RELATED LINKS</span></span>
