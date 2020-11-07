---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795193"
---
# <span data-ttu-id="9a04a-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9a04a-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="9a04a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a04a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a04a-103">修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="9a04a-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="9a04a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a04a-104">SYNTAX</span></span>

### <span data-ttu-id="9a04a-105">BySpecifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="9a04a-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a04a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a04a-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a04a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="9a04a-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a04a-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="9a04a-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a04a-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9a04a-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a04a-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9a04a-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a04a-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="9a04a-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a04a-112">說明</span><span class="sxs-lookup"><span data-stu-id="9a04a-112">DESCRIPTION</span></span>
<span data-ttu-id="9a04a-113">**AzResourceLock** Cmdlet 會修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="9a04a-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="9a04a-114">示例</span><span class="sxs-lookup"><span data-stu-id="9a04a-114">EXAMPLES</span></span>

### <span data-ttu-id="9a04a-115">範例1：更新鎖定的筆記</span><span class="sxs-lookup"><span data-stu-id="9a04a-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9a04a-116">這個命令會更新名為 ContosoSiteLock 之鎖定的筆記。</span><span class="sxs-lookup"><span data-stu-id="9a04a-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="9a04a-117">參數</span><span class="sxs-lookup"><span data-stu-id="9a04a-117">PARAMETERS</span></span>

### <span data-ttu-id="9a04a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9a04a-118">-ApiVersion</span></span>
<span data-ttu-id="9a04a-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9a04a-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9a04a-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="9a04a-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9a04a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a04a-121">-DefaultProfile</span></span>
<span data-ttu-id="9a04a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9a04a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a04a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9a04a-123">-Force</span></span>
<span data-ttu-id="9a04a-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9a04a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a04a-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9a04a-125">-InformationAction</span></span>
<span data-ttu-id="9a04a-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9a04a-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="9a04a-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a04a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a04a-128">持續</span><span class="sxs-lookup"><span data-stu-id="9a04a-128">Continue</span></span>
- <span data-ttu-id="9a04a-129">理會</span><span class="sxs-lookup"><span data-stu-id="9a04a-129">Ignore</span></span>
- <span data-ttu-id="9a04a-130">看</span><span class="sxs-lookup"><span data-stu-id="9a04a-130">Inquire</span></span>
- <span data-ttu-id="9a04a-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9a04a-131">SilentlyContinue</span></span>
- <span data-ttu-id="9a04a-132">停止</span><span class="sxs-lookup"><span data-stu-id="9a04a-132">Stop</span></span>
- <span data-ttu-id="9a04a-133">封存</span><span class="sxs-lookup"><span data-stu-id="9a04a-133">Suspend</span></span>

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

### <span data-ttu-id="9a04a-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9a04a-134">-InformationVariable</span></span>
<span data-ttu-id="9a04a-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9a04a-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9a04a-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="9a04a-136">-LockId</span></span>
<span data-ttu-id="9a04a-137">指定此 Cmdlet 所修改之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a04a-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9a04a-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="9a04a-138">-LockLevel</span></span>
<span data-ttu-id="9a04a-139">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="9a04a-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="9a04a-140">目前唯一有效的值是 CanNotDelete。</span><span class="sxs-lookup"><span data-stu-id="9a04a-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a04a-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="9a04a-141">-LockName</span></span>
<span data-ttu-id="9a04a-142">指定此 Cmdlet 修改的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="9a04a-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a04a-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="9a04a-143">-LockNotes</span></span>
<span data-ttu-id="9a04a-144">指定鎖定的備忘稿。</span><span class="sxs-lookup"><span data-stu-id="9a04a-144">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a04a-145">-預先</span><span class="sxs-lookup"><span data-stu-id="9a04a-145">-Pre</span></span>
<span data-ttu-id="9a04a-146">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9a04a-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9a04a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a04a-147">-ResourceGroupName</span></span>
<span data-ttu-id="9a04a-148">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a04a-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="9a04a-149">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="9a04a-149">-ResourceName</span></span>
<span data-ttu-id="9a04a-150">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a04a-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9a04a-151">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="9a04a-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="9a04a-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9a04a-152">-ResourceType</span></span>
<span data-ttu-id="9a04a-153">指定要套用鎖定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="9a04a-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="9a04a-154">-範圍</span><span class="sxs-lookup"><span data-stu-id="9a04a-154">-Scope</span></span>
<span data-ttu-id="9a04a-155">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="9a04a-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="9a04a-156">例如，若要指定資料庫，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱 `/providers/Microsoft.Sql/servers/` 伺服器名稱 `/databases/` 資料庫名稱若要指定資源群組，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱</span><span class="sxs-lookup"><span data-stu-id="9a04a-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="9a04a-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9a04a-157">-TenantLevel</span></span>
<span data-ttu-id="9a04a-158">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="9a04a-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9a04a-159">-確認</span><span class="sxs-lookup"><span data-stu-id="9a04a-159">-Confirm</span></span>
<span data-ttu-id="9a04a-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a04a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a04a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a04a-161">-WhatIf</span></span>
<span data-ttu-id="9a04a-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a04a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a04a-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a04a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a04a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a04a-164">CommonParameters</span></span>
<span data-ttu-id="9a04a-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a04a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a04a-166">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a04a-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a04a-167">輸入</span><span class="sxs-lookup"><span data-stu-id="9a04a-167">INPUTS</span></span>

## <span data-ttu-id="9a04a-168">輸出</span><span class="sxs-lookup"><span data-stu-id="9a04a-168">OUTPUTS</span></span>

## <span data-ttu-id="9a04a-169">筆記</span><span class="sxs-lookup"><span data-stu-id="9a04a-169">NOTES</span></span>

## <span data-ttu-id="9a04a-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a04a-170">RELATED LINKS</span></span>

[<span data-ttu-id="9a04a-171">AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9a04a-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="9a04a-172">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9a04a-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="9a04a-173">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="9a04a-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


