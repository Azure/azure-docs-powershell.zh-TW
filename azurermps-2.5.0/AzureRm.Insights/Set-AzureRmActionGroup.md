---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800141"
---
# <span data-ttu-id="12758-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="12758-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="12758-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12758-102">SYNOPSIS</span></span>
<span data-ttu-id="12758-103">建立新的或更新現有的動作群組。</span><span class="sxs-lookup"><span data-stu-id="12758-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12758-104">句法</span><span class="sxs-lookup"><span data-stu-id="12758-104">SYNTAX</span></span>

### <span data-ttu-id="12758-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="12758-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12758-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12758-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12758-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12758-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12758-108">說明</span><span class="sxs-lookup"><span data-stu-id="12758-108">DESCRIPTION</span></span>
<span data-ttu-id="12758-109">**AzureRmActionGroup** Cmdlet 會建立新的或更新現有的動作群組</span><span class="sxs-lookup"><span data-stu-id="12758-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="12758-110">示例</span><span class="sxs-lookup"><span data-stu-id="12758-110">EXAMPLES</span></span>

### <span data-ttu-id="12758-111">範例1：建立動作群組</span><span class="sxs-lookup"><span data-stu-id="12758-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="12758-112">前兩個命令會建立兩個接收方。</span><span class="sxs-lookup"><span data-stu-id="12758-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="12758-113">最後一個命令會建立包含兩個接收器的動作群組。</span><span class="sxs-lookup"><span data-stu-id="12758-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="12758-114">參數</span><span class="sxs-lookup"><span data-stu-id="12758-114">PARAMETERS</span></span>

### <span data-ttu-id="12758-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12758-115">-DefaultProfile</span></span>
<span data-ttu-id="12758-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="12758-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12758-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="12758-117">-DisableGroup</span></span>
<span data-ttu-id="12758-118">停用 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="12758-118">Disables the action group.</span></span>

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

### <span data-ttu-id="12758-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12758-119">-InputObject</span></span>
<span data-ttu-id="12758-120">[動作] 群組 resourc</span><span class="sxs-lookup"><span data-stu-id="12758-120">The action group resourc</span></span>

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

### <span data-ttu-id="12758-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="12758-121">-Name</span></span>
<span data-ttu-id="12758-122">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12758-122">The name of the action group.</span></span>

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

### <span data-ttu-id="12758-123">-接收器</span><span class="sxs-lookup"><span data-stu-id="12758-123">-Receiver</span></span>
<span data-ttu-id="12758-124">動作群組的接收器清單。</span><span class="sxs-lookup"><span data-stu-id="12758-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="12758-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12758-125">-ResourceGroupName</span></span>
<span data-ttu-id="12758-126">資源群組</span><span class="sxs-lookup"><span data-stu-id="12758-126">The resource group nam</span></span>

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

### <span data-ttu-id="12758-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12758-127">-ResourceId</span></span>
<span data-ttu-id="12758-128">資源 i</span><span class="sxs-lookup"><span data-stu-id="12758-128">The resource i</span></span>

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

### <span data-ttu-id="12758-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="12758-129">-ShortName</span></span>
<span data-ttu-id="12758-130">動作群組的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="12758-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="12758-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="12758-131">-Tag</span></span>
<span data-ttu-id="12758-132">[動作] 群組 resourc 的標記</span><span class="sxs-lookup"><span data-stu-id="12758-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="12758-133">-確認</span><span class="sxs-lookup"><span data-stu-id="12758-133">-Confirm</span></span>
<span data-ttu-id="12758-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12758-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12758-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12758-135">-WhatIf</span></span>
<span data-ttu-id="12758-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12758-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12758-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12758-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12758-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12758-138">CommonParameters</span></span>
<span data-ttu-id="12758-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12758-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12758-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12758-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12758-141">輸入</span><span class="sxs-lookup"><span data-stu-id="12758-141">INPUTS</span></span>

### <span data-ttu-id="12758-142">System.object</span><span class="sxs-lookup"><span data-stu-id="12758-142">System.String</span></span>

### <span data-ttu-id="12758-143">[System.object]。清單 ' 1 [OutputClasses. PSActionGroupReceiverBase，5.1.0.0，命令資訊，版本 =，Culture = 中性，PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="12758-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="12758-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="12758-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="12758-145">System.object. IDictionary "2 [（System.object，字串，mscorlib.dll，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]，[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="12758-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="12758-146">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="12758-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="12758-147">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="12758-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="12758-148">輸出</span><span class="sxs-lookup"><span data-stu-id="12758-148">OUTPUTS</span></span>

### <span data-ttu-id="12758-149">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="12758-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="12758-150">筆記</span><span class="sxs-lookup"><span data-stu-id="12758-150">NOTES</span></span>

## <span data-ttu-id="12758-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="12758-151">RELATED LINKS</span></span>

<span data-ttu-id="12758-152">[AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="12758-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
