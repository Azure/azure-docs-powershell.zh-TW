---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: b4f509d6ba688cab993f83cd0b094b3f8394d36f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446239"
---
# <span data-ttu-id="d7e89-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="d7e89-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="d7e89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7e89-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e89-103">建立新的或更新現有的動作群組。</span><span class="sxs-lookup"><span data-stu-id="d7e89-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7e89-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7e89-104">SYNTAX</span></span>

### <span data-ttu-id="d7e89-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="d7e89-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e89-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7e89-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e89-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7e89-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7e89-108">說明</span><span class="sxs-lookup"><span data-stu-id="d7e89-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e89-109">**AzureRmActionGroup** Cmdlet 會建立新的或更新現有的動作群組</span><span class="sxs-lookup"><span data-stu-id="d7e89-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="d7e89-110">示例</span><span class="sxs-lookup"><span data-stu-id="d7e89-110">EXAMPLES</span></span>

### <span data-ttu-id="d7e89-111">範例1：建立動作群組</span><span class="sxs-lookup"><span data-stu-id="d7e89-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="d7e89-112">前兩個命令會建立兩個接收方。</span><span class="sxs-lookup"><span data-stu-id="d7e89-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="d7e89-113">最後一個命令會建立包含兩個接收器的動作群組。</span><span class="sxs-lookup"><span data-stu-id="d7e89-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="d7e89-114">參數</span><span class="sxs-lookup"><span data-stu-id="d7e89-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e89-115">-DefaultProfile</span></span>
<span data-ttu-id="d7e89-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d7e89-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="d7e89-117">-DisableGroup</span></span>
<span data-ttu-id="d7e89-118">停用 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="d7e89-118">Disables the action group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7e89-119">-InputObject</span></span>
<span data-ttu-id="d7e89-120">[動作] 群組 resourc</span><span class="sxs-lookup"><span data-stu-id="d7e89-120">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7e89-121">-Name</span></span>
<span data-ttu-id="d7e89-122">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7e89-122">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-123">-接收器</span><span class="sxs-lookup"><span data-stu-id="d7e89-123">-Receiver</span></span>
<span data-ttu-id="d7e89-124">動作群組的接收器清單。</span><span class="sxs-lookup"><span data-stu-id="d7e89-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="d7e89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e89-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7e89-126">資源群組</span><span class="sxs-lookup"><span data-stu-id="d7e89-126">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7e89-127">-ResourceId</span></span>
<span data-ttu-id="d7e89-128">資源 i</span><span class="sxs-lookup"><span data-stu-id="d7e89-128">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="d7e89-129">-ShortName</span></span>
<span data-ttu-id="d7e89-130">動作群組的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="d7e89-130">The short name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7e89-131">-Tag</span></span>
<span data-ttu-id="d7e89-132">[動作] 群組 resourc 的標記</span><span class="sxs-lookup"><span data-stu-id="d7e89-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="d7e89-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d7e89-133">-Confirm</span></span>
<span data-ttu-id="d7e89-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d7e89-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e89-135">-WhatIf</span></span>
<span data-ttu-id="d7e89-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7e89-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7e89-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7e89-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e89-138">CommonParameters</span></span>
<span data-ttu-id="d7e89-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7e89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e89-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7e89-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e89-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d7e89-141">INPUTS</span></span>

### <span data-ttu-id="d7e89-142">所有</span><span class="sxs-lookup"><span data-stu-id="d7e89-142">None</span></span>
<span data-ttu-id="d7e89-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d7e89-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7e89-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d7e89-144">OUTPUTS</span></span>

### <span data-ttu-id="d7e89-145">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="d7e89-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="d7e89-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d7e89-146">NOTES</span></span>

## <span data-ttu-id="d7e89-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7e89-147">RELATED LINKS</span></span>

<span data-ttu-id="d7e89-148">[AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="d7e89-148">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
