---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452492"
---
# <span data-ttu-id="05253-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="05253-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="05253-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05253-102">SYNOPSIS</span></span>
<span data-ttu-id="05253-103">建立新的或更新現有的動作群組。</span><span class="sxs-lookup"><span data-stu-id="05253-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05253-104">句法</span><span class="sxs-lookup"><span data-stu-id="05253-104">SYNTAX</span></span>

### <span data-ttu-id="05253-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="05253-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05253-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05253-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05253-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05253-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05253-108">說明</span><span class="sxs-lookup"><span data-stu-id="05253-108">DESCRIPTION</span></span>
<span data-ttu-id="05253-109">**AzureRmActionGroup** Cmdlet 會建立新的或更新現有的動作群組</span><span class="sxs-lookup"><span data-stu-id="05253-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="05253-110">示例</span><span class="sxs-lookup"><span data-stu-id="05253-110">EXAMPLES</span></span>

### <span data-ttu-id="05253-111">範例1：建立動作群組</span><span class="sxs-lookup"><span data-stu-id="05253-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="05253-112">前兩個命令會建立兩個接收方。</span><span class="sxs-lookup"><span data-stu-id="05253-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="05253-113">最後一個命令會建立包含兩個接收器的動作群組。</span><span class="sxs-lookup"><span data-stu-id="05253-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="05253-114">參數</span><span class="sxs-lookup"><span data-stu-id="05253-114">PARAMETERS</span></span>

### <span data-ttu-id="05253-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="05253-115">-Name</span></span>
<span data-ttu-id="05253-116">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05253-116">The name of the action group.</span></span>

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

### <span data-ttu-id="05253-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="05253-117">-ShortName</span></span>
<span data-ttu-id="05253-118">動作群組的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="05253-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="05253-119">-接收器</span><span class="sxs-lookup"><span data-stu-id="05253-119">-Receiver</span></span>
<span data-ttu-id="05253-120">動作群組的接收器清單。</span><span class="sxs-lookup"><span data-stu-id="05253-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="05253-121">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="05253-121">-DisableGroup</span></span>
<span data-ttu-id="05253-122">停用 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="05253-122">Disables the action group.</span></span>

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

### <span data-ttu-id="05253-123">-確認</span><span class="sxs-lookup"><span data-stu-id="05253-123">-Confirm</span></span>
<span data-ttu-id="05253-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05253-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05253-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05253-125">-DefaultProfile</span></span>
<span data-ttu-id="05253-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05253-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05253-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05253-127">-InputObject</span></span>
<span data-ttu-id="05253-128">[動作] 群組資源</span><span class="sxs-lookup"><span data-stu-id="05253-128">The action group resource</span></span>

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

### <span data-ttu-id="05253-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05253-129">-ResourceGroupName</span></span>
<span data-ttu-id="05253-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="05253-130">The resource group name</span></span>

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

### <span data-ttu-id="05253-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05253-131">-ResourceId</span></span>
<span data-ttu-id="05253-132">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="05253-132">The resource id</span></span>

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

### <span data-ttu-id="05253-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="05253-133">-Tag</span></span>
<span data-ttu-id="05253-134">[動作] 群組資源的標記</span><span class="sxs-lookup"><span data-stu-id="05253-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="05253-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05253-135">-WhatIf</span></span>
<span data-ttu-id="05253-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05253-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05253-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05253-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05253-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05253-138">CommonParameters</span></span>
<span data-ttu-id="05253-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05253-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05253-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05253-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05253-141">輸入</span><span class="sxs-lookup"><span data-stu-id="05253-141">INPUTS</span></span>

## <span data-ttu-id="05253-142">輸出</span><span class="sxs-lookup"><span data-stu-id="05253-142">OUTPUTS</span></span>

### <span data-ttu-id="05253-143">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="05253-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="05253-144">筆記</span><span class="sxs-lookup"><span data-stu-id="05253-144">NOTES</span></span>

## <span data-ttu-id="05253-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="05253-145">RELATED LINKS</span></span>

<span data-ttu-id="05253-146">[AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
[新-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="05253-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
