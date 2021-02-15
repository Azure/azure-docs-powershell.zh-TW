---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: ede2a8566f7305b4f56a5fc392090b426c148547
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399000"
---
# <span data-ttu-id="2964e-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2964e-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="2964e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2964e-102">SYNOPSIS</span></span>
<span data-ttu-id="2964e-103">建立新動作或更新現有的動作群組。</span><span class="sxs-lookup"><span data-stu-id="2964e-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="2964e-104">語法</span><span class="sxs-lookup"><span data-stu-id="2964e-104">SYNTAX</span></span>

### <span data-ttu-id="2964e-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="2964e-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2964e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2964e-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2964e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2964e-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2964e-108">描述</span><span class="sxs-lookup"><span data-stu-id="2964e-108">DESCRIPTION</span></span>
<span data-ttu-id="2964e-109">**Set-AzActionGroup** Cmdlet 會建立新動作群組或更新現有動作群組</span><span class="sxs-lookup"><span data-stu-id="2964e-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="2964e-110">例子</span><span class="sxs-lookup"><span data-stu-id="2964e-110">EXAMPLES</span></span>

### <span data-ttu-id="2964e-111">範例 1：建立動作群組</span><span class="sxs-lookup"><span data-stu-id="2964e-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="2964e-112">前兩個命令會建立兩個收聽者。</span><span class="sxs-lookup"><span data-stu-id="2964e-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="2964e-113">最後一個命令會建立一個動作群組，包括兩個收受者。</span><span class="sxs-lookup"><span data-stu-id="2964e-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="2964e-114">參數</span><span class="sxs-lookup"><span data-stu-id="2964e-114">PARAMETERS</span></span>

### <span data-ttu-id="2964e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2964e-115">-DefaultProfile</span></span>
<span data-ttu-id="2964e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2964e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2964e-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="2964e-117">-DisableGroup</span></span>
<span data-ttu-id="2964e-118">停用動作群組。</span><span class="sxs-lookup"><span data-stu-id="2964e-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2964e-119">-InputObject</span></span>
<span data-ttu-id="2964e-120">動作群組資源</span><span class="sxs-lookup"><span data-stu-id="2964e-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2964e-121">-Name</span></span>
<span data-ttu-id="2964e-122">動作組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2964e-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="2964e-123">-Receiver</span></span>
<span data-ttu-id="2964e-124">動作群組的收受者清單。</span><span class="sxs-lookup"><span data-stu-id="2964e-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2964e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2964e-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2964e-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2964e-127">-ResourceId</span></span>
<span data-ttu-id="2964e-128">資源 i</span><span class="sxs-lookup"><span data-stu-id="2964e-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="2964e-129">-ShortName</span></span>
<span data-ttu-id="2964e-130">動作群組的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="2964e-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-131">-標記</span><span class="sxs-lookup"><span data-stu-id="2964e-131">-Tag</span></span>
<span data-ttu-id="2964e-132">動作群組資源的標記</span><span class="sxs-lookup"><span data-stu-id="2964e-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2964e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2964e-133">-Confirm</span></span>
<span data-ttu-id="2964e-134">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2964e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2964e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2964e-135">-WhatIf</span></span>
<span data-ttu-id="2964e-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2964e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2964e-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2964e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2964e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2964e-138">CommonParameters</span></span>
<span data-ttu-id="2964e-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2964e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2964e-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2964e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2964e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2964e-141">INPUTS</span></span>

### <span data-ttu-id="2964e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2964e-142">System.String</span></span>

### <span data-ttu-id="2964e-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2964e-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2964e-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2964e-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2964e-145">System.Collections.generic.IDictionary'2[System.String， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]，[System.String， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2964e-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2964e-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2964e-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2964e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="2964e-147">OUTPUTS</span></span>

### <span data-ttu-id="2964e-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2964e-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2964e-149">筆記</span><span class="sxs-lookup"><span data-stu-id="2964e-149">NOTES</span></span>

## <span data-ttu-id="2964e-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="2964e-150">RELATED LINKS</span></span>

<span data-ttu-id="2964e-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="2964e-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

