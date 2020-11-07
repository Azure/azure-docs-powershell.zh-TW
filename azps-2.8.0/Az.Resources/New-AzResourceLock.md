---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792212"
---
# <span data-ttu-id="92cc7-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="92cc7-101">New-AzResourceLock</span></span>

## <span data-ttu-id="92cc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="92cc7-103">建立資源鎖。</span><span class="sxs-lookup"><span data-stu-id="92cc7-103">Creates a resource lock.</span></span>

## <span data-ttu-id="92cc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="92cc7-104">SYNTAX</span></span>

### <span data-ttu-id="92cc7-105">BySpecifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="92cc7-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92cc7-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92cc7-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cc7-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="92cc7-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cc7-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="92cc7-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92cc7-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="92cc7-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cc7-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="92cc7-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cc7-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="92cc7-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92cc7-112">說明</span><span class="sxs-lookup"><span data-stu-id="92cc7-112">DESCRIPTION</span></span>
<span data-ttu-id="92cc7-113">**新的-AzResourceLock** Cmdlet 會建立資源鎖。</span><span class="sxs-lookup"><span data-stu-id="92cc7-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="92cc7-114">示例</span><span class="sxs-lookup"><span data-stu-id="92cc7-114">EXAMPLES</span></span>

### <span data-ttu-id="92cc7-115">範例1：在網站上建立資源鎖定</span><span class="sxs-lookup"><span data-stu-id="92cc7-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="92cc7-116">這個命令會在網站上建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="92cc7-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="92cc7-117">參數</span><span class="sxs-lookup"><span data-stu-id="92cc7-117">PARAMETERS</span></span>

### <span data-ttu-id="92cc7-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92cc7-118">-ApiVersion</span></span>
<span data-ttu-id="92cc7-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="92cc7-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="92cc7-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="92cc7-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="92cc7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cc7-121">-DefaultProfile</span></span>
<span data-ttu-id="92cc7-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="92cc7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92cc7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="92cc7-123">-Force</span></span>
<span data-ttu-id="92cc7-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="92cc7-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92cc7-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="92cc7-125">-LockId</span></span>
<span data-ttu-id="92cc7-126">指定鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="92cc7-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="92cc7-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="92cc7-127">-LockLevel</span></span>
<span data-ttu-id="92cc7-128">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="92cc7-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="92cc7-129">目前，有效值為 CanNotDelete、ReadOnly。</span><span class="sxs-lookup"><span data-stu-id="92cc7-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92cc7-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="92cc7-130">-LockName</span></span>
<span data-ttu-id="92cc7-131">指定鎖定的名稱。</span><span class="sxs-lookup"><span data-stu-id="92cc7-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="92cc7-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="92cc7-132">-LockNotes</span></span>
<span data-ttu-id="92cc7-133">指定鎖定的備忘稿。</span><span class="sxs-lookup"><span data-stu-id="92cc7-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="92cc7-134">-預先</span><span class="sxs-lookup"><span data-stu-id="92cc7-134">-Pre</span></span>
<span data-ttu-id="92cc7-135">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="92cc7-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="92cc7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92cc7-136">-ResourceGroupName</span></span>
<span data-ttu-id="92cc7-137">指定鎖定適用之資源群組的名稱，或包含該鎖定所套用之資源群組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92cc7-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="92cc7-138">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="92cc7-138">-ResourceName</span></span>
<span data-ttu-id="92cc7-139">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="92cc7-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="92cc7-140">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="92cc7-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="92cc7-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="92cc7-141">-ResourceType</span></span>
<span data-ttu-id="92cc7-142">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="92cc7-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="92cc7-143">-範圍</span><span class="sxs-lookup"><span data-stu-id="92cc7-143">-Scope</span></span>
<span data-ttu-id="92cc7-144">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="92cc7-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="92cc7-145">例如，若要指定資料庫，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱 `/providers/Microsoft.Sql/servers/` 伺服器名稱 `/databases/` 資料庫名稱若要指定資源群組，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱</span><span class="sxs-lookup"><span data-stu-id="92cc7-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="92cc7-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="92cc7-146">-TenantLevel</span></span>
<span data-ttu-id="92cc7-147">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="92cc7-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="92cc7-148">-確認</span><span class="sxs-lookup"><span data-stu-id="92cc7-148">-Confirm</span></span>
<span data-ttu-id="92cc7-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92cc7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92cc7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92cc7-150">-WhatIf</span></span>
<span data-ttu-id="92cc7-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92cc7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92cc7-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92cc7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92cc7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cc7-153">CommonParameters</span></span>
<span data-ttu-id="92cc7-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92cc7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cc7-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92cc7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cc7-156">輸入</span><span class="sxs-lookup"><span data-stu-id="92cc7-156">INPUTS</span></span>

### <span data-ttu-id="92cc7-157">System.object</span><span class="sxs-lookup"><span data-stu-id="92cc7-157">System.String</span></span>

### <span data-ttu-id="92cc7-158">LockLevel 中的 [.] 命令。</span><span class="sxs-lookup"><span data-stu-id="92cc7-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="92cc7-159">輸出</span><span class="sxs-lookup"><span data-stu-id="92cc7-159">OUTPUTS</span></span>

### <span data-ttu-id="92cc7-160">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="92cc7-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="92cc7-161">筆記</span><span class="sxs-lookup"><span data-stu-id="92cc7-161">NOTES</span></span>

## <span data-ttu-id="92cc7-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="92cc7-162">RELATED LINKS</span></span>

[<span data-ttu-id="92cc7-163">AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="92cc7-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="92cc7-164">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="92cc7-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="92cc7-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="92cc7-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


