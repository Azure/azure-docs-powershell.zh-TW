---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795220"
---
# <span data-ttu-id="27e68-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="27e68-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="27e68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27e68-102">SYNOPSIS</span></span>
<span data-ttu-id="27e68-103">移除資源鎖。</span><span class="sxs-lookup"><span data-stu-id="27e68-103">Removes a resource lock.</span></span>

## <span data-ttu-id="27e68-104">句法</span><span class="sxs-lookup"><span data-stu-id="27e68-104">SYNTAX</span></span>

### <span data-ttu-id="27e68-105">ByLockId (預設) </span><span class="sxs-lookup"><span data-stu-id="27e68-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e68-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27e68-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e68-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="27e68-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27e68-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="27e68-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e68-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="27e68-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e68-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="27e68-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27e68-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="27e68-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27e68-112">說明</span><span class="sxs-lookup"><span data-stu-id="27e68-112">DESCRIPTION</span></span>
<span data-ttu-id="27e68-113">**AzResourceLock** Cmdlet 會移除 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="27e68-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="27e68-114">示例</span><span class="sxs-lookup"><span data-stu-id="27e68-114">EXAMPLES</span></span>

### <span data-ttu-id="27e68-115">範例1：移除鎖定</span><span class="sxs-lookup"><span data-stu-id="27e68-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="27e68-116">這個命令會移除名為 ContosoSiteLock 的鎖定。</span><span class="sxs-lookup"><span data-stu-id="27e68-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="27e68-117">參數</span><span class="sxs-lookup"><span data-stu-id="27e68-117">PARAMETERS</span></span>

### <span data-ttu-id="27e68-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="27e68-118">-ApiVersion</span></span>
<span data-ttu-id="27e68-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="27e68-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="27e68-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="27e68-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="27e68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e68-121">-DefaultProfile</span></span>
<span data-ttu-id="27e68-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="27e68-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-123">-Force</span><span class="sxs-lookup"><span data-stu-id="27e68-123">-Force</span></span>
<span data-ttu-id="27e68-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="27e68-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27e68-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="27e68-125">-InformationAction</span></span>
<span data-ttu-id="27e68-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="27e68-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="27e68-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="27e68-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27e68-128">持續</span><span class="sxs-lookup"><span data-stu-id="27e68-128">Continue</span></span>
- <span data-ttu-id="27e68-129">理會</span><span class="sxs-lookup"><span data-stu-id="27e68-129">Ignore</span></span>
- <span data-ttu-id="27e68-130">看</span><span class="sxs-lookup"><span data-stu-id="27e68-130">Inquire</span></span>
- <span data-ttu-id="27e68-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="27e68-131">SilentlyContinue</span></span>
- <span data-ttu-id="27e68-132">停止</span><span class="sxs-lookup"><span data-stu-id="27e68-132">Stop</span></span>
- <span data-ttu-id="27e68-133">封存</span><span class="sxs-lookup"><span data-stu-id="27e68-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="27e68-134">-InformationVariable</span></span>
<span data-ttu-id="27e68-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="27e68-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="27e68-136">-LockId</span></span>
<span data-ttu-id="27e68-137">指定此 Cmdlet 移除之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27e68-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="27e68-138">-LockName</span></span>
<span data-ttu-id="27e68-139">指定此 Cmdlet 移除的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="27e68-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-140">-預先</span><span class="sxs-lookup"><span data-stu-id="27e68-140">-Pre</span></span>
<span data-ttu-id="27e68-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="27e68-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="27e68-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e68-142">-ResourceGroupName</span></span>
<span data-ttu-id="27e68-143">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e68-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-144">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="27e68-144">-ResourceName</span></span>
<span data-ttu-id="27e68-145">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e68-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="27e68-146">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="27e68-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="27e68-147">-ResourceType</span></span>
<span data-ttu-id="27e68-148">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="27e68-148">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-149">-範圍</span><span class="sxs-lookup"><span data-stu-id="27e68-149">-Scope</span></span>
<span data-ttu-id="27e68-150">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="27e68-150">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="27e68-151">-TenantLevel</span></span>
<span data-ttu-id="27e68-152">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="27e68-152">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-153">-確認</span><span class="sxs-lookup"><span data-stu-id="27e68-153">-Confirm</span></span>
<span data-ttu-id="27e68-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27e68-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e68-155">-WhatIf</span></span>
<span data-ttu-id="27e68-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27e68-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27e68-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27e68-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e68-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e68-158">CommonParameters</span></span>
<span data-ttu-id="27e68-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27e68-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e68-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27e68-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e68-161">輸入</span><span class="sxs-lookup"><span data-stu-id="27e68-161">INPUTS</span></span>

## <span data-ttu-id="27e68-162">輸出</span><span class="sxs-lookup"><span data-stu-id="27e68-162">OUTPUTS</span></span>

## <span data-ttu-id="27e68-163">筆記</span><span class="sxs-lookup"><span data-stu-id="27e68-163">NOTES</span></span>

## <span data-ttu-id="27e68-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="27e68-164">RELATED LINKS</span></span>

[<span data-ttu-id="27e68-165">AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="27e68-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="27e68-166">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="27e68-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="27e68-167">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="27e68-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


