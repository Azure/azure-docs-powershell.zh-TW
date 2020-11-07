---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792134"
---
# <span data-ttu-id="f551a-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="f551a-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="f551a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f551a-102">SYNOPSIS</span></span>
<span data-ttu-id="f551a-103">更新安全警示狀態。</span><span class="sxs-lookup"><span data-stu-id="f551a-103">Updates a security alert state.</span></span>

## <span data-ttu-id="f551a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f551a-104">SYNTAX</span></span>

### <span data-ttu-id="f551a-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f551a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f551a-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f551a-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f551a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f551a-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f551a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="f551a-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f551a-109">說明</span><span class="sxs-lookup"><span data-stu-id="f551a-109">DESCRIPTION</span></span>
<span data-ttu-id="f551a-110">設定安全性警示狀態。</span><span class="sxs-lookup"><span data-stu-id="f551a-110">Sets a security alert state.</span></span>

## <span data-ttu-id="f551a-111">示例</span><span class="sxs-lookup"><span data-stu-id="f551a-111">EXAMPLES</span></span>

### <span data-ttu-id="f551a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f551a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="f551a-113">關閉引發的安全性警示。</span><span class="sxs-lookup"><span data-stu-id="f551a-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="f551a-114">參數</span><span class="sxs-lookup"><span data-stu-id="f551a-114">PARAMETERS</span></span>

### <span data-ttu-id="f551a-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="f551a-115">-ActionType</span></span>
<span data-ttu-id="f551a-116">動作類型。</span><span class="sxs-lookup"><span data-stu-id="f551a-116">Action Type.</span></span>

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

### <span data-ttu-id="f551a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f551a-117">-DefaultProfile</span></span>
<span data-ttu-id="f551a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f551a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f551a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f551a-119">-InputObject</span></span>
<span data-ttu-id="f551a-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="f551a-120">Input Object.</span></span>

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

### <span data-ttu-id="f551a-121">-位置</span><span class="sxs-lookup"><span data-stu-id="f551a-121">-Location</span></span>
<span data-ttu-id="f551a-122">位於.</span><span class="sxs-lookup"><span data-stu-id="f551a-122">Location.</span></span>

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

### <span data-ttu-id="f551a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f551a-123">-Name</span></span>
<span data-ttu-id="f551a-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f551a-124">Resource name.</span></span>

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

### <span data-ttu-id="f551a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f551a-125">-PassThru</span></span>
<span data-ttu-id="f551a-126">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="f551a-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f551a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f551a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f551a-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f551a-128">Resource group name.</span></span>

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

### <span data-ttu-id="f551a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f551a-129">-ResourceId</span></span>
<span data-ttu-id="f551a-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f551a-130">Resource ID.</span></span>

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

### <span data-ttu-id="f551a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f551a-131">-Confirm</span></span>
<span data-ttu-id="f551a-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f551a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f551a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f551a-133">-WhatIf</span></span>
<span data-ttu-id="f551a-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f551a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f551a-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f551a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f551a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f551a-136">CommonParameters</span></span>
<span data-ttu-id="f551a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f551a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f551a-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f551a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f551a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f551a-139">INPUTS</span></span>

### <span data-ttu-id="f551a-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f551a-140">System.String</span></span>

### <span data-ttu-id="f551a-141">PSSecurityAlert （Security. 命令）。</span><span class="sxs-lookup"><span data-stu-id="f551a-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="f551a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f551a-142">OUTPUTS</span></span>

### <span data-ttu-id="f551a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f551a-143">System.Boolean</span></span>

## <span data-ttu-id="f551a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f551a-144">NOTES</span></span>

## <span data-ttu-id="f551a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f551a-145">RELATED LINKS</span></span>
