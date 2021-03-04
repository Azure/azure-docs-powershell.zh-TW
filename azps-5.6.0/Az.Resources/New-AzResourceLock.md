---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 630ea593304523572403fce0db3d6118be66403f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906513"
---
# <span data-ttu-id="bd23e-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd23e-101">New-AzResourceLock</span></span>

## <span data-ttu-id="bd23e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd23e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd23e-103">建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bd23e-103">Creates a resource lock.</span></span>

## <span data-ttu-id="bd23e-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd23e-104">SYNTAX</span></span>

### <span data-ttu-id="bd23e-105">BySifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="bd23e-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd23e-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd23e-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd23e-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bd23e-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd23e-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bd23e-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd23e-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bd23e-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd23e-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="bd23e-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd23e-111">描述</span><span class="sxs-lookup"><span data-stu-id="bd23e-111">DESCRIPTION</span></span>
<span data-ttu-id="bd23e-112">**New-AzResourceLock** Cmdlet 會建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bd23e-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="bd23e-113">例子</span><span class="sxs-lookup"><span data-stu-id="bd23e-113">EXAMPLES</span></span>

### <span data-ttu-id="bd23e-114">範例 1：在網站上建立資源鎖定</span><span class="sxs-lookup"><span data-stu-id="bd23e-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="bd23e-115">此命令會在網站上建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bd23e-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="bd23e-116">範例 2：在資料庫上建立資源鎖定</span><span class="sxs-lookup"><span data-stu-id="bd23e-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="bd23e-117">此命令在 Azure 資料庫上建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bd23e-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="bd23e-118">參數</span><span class="sxs-lookup"><span data-stu-id="bd23e-118">PARAMETERS</span></span>

### <span data-ttu-id="bd23e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bd23e-119">-ApiVersion</span></span>
<span data-ttu-id="bd23e-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bd23e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bd23e-121">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="bd23e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bd23e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd23e-122">-DefaultProfile</span></span>
<span data-ttu-id="bd23e-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bd23e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd23e-124">-強制</span><span class="sxs-lookup"><span data-stu-id="bd23e-124">-Force</span></span>
<span data-ttu-id="bd23e-125">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bd23e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd23e-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="bd23e-126">-LockId</span></span>
<span data-ttu-id="bd23e-127">指定鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd23e-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="bd23e-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="bd23e-128">-LockLevel</span></span>
<span data-ttu-id="bd23e-129">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="bd23e-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="bd23e-130">目前，有效的值為 CanNotDelete、ReadOnly。</span><span class="sxs-lookup"><span data-stu-id="bd23e-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="bd23e-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="bd23e-131">-LockName</span></span>
<span data-ttu-id="bd23e-132">指定鎖定的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd23e-132">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd23e-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="bd23e-133">-LockNotes</span></span>
<span data-ttu-id="bd23e-134">指定鎖定的附注。</span><span class="sxs-lookup"><span data-stu-id="bd23e-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="bd23e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd23e-135">-Pre</span></span>
<span data-ttu-id="bd23e-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bd23e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bd23e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd23e-137">-ResourceGroupName</span></span>
<span data-ttu-id="bd23e-138">指定鎖定所適用之資源組的名稱，或包含該鎖定所適用之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd23e-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="bd23e-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bd23e-139">-ResourceName</span></span>
<span data-ttu-id="bd23e-140">指定鎖定所適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd23e-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bd23e-141">例如，若要指定資料庫，請使用下列格式： `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="bd23e-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd23e-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bd23e-142">-ResourceType</span></span>
<span data-ttu-id="bd23e-143">指定鎖定所適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="bd23e-143">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd23e-144">-範圍</span><span class="sxs-lookup"><span data-stu-id="bd23e-144">-Scope</span></span>
<span data-ttu-id="bd23e-145">指定鎖定所適用的範圍。</span><span class="sxs-lookup"><span data-stu-id="bd23e-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="bd23e-146">例如，若要指定資料庫，請使用下列格式：訂閱識別碼資源組名伺服器名稱資料庫名稱若要指定資源群組，請使用下列格式 `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` ： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名</span><span class="sxs-lookup"><span data-stu-id="bd23e-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="bd23e-147">-確認</span><span class="sxs-lookup"><span data-stu-id="bd23e-147">-Confirm</span></span>
<span data-ttu-id="bd23e-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd23e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd23e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd23e-149">-WhatIf</span></span>
<span data-ttu-id="bd23e-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd23e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd23e-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd23e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd23e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd23e-152">CommonParameters</span></span>
<span data-ttu-id="bd23e-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd23e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd23e-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd23e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd23e-155">輸入</span><span class="sxs-lookup"><span data-stu-id="bd23e-155">INPUTS</span></span>

### <span data-ttu-id="bd23e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="bd23e-156">System.String</span></span>

### <span data-ttu-id="bd23e-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Lock.LockLevel</span><span class="sxs-lookup"><span data-stu-id="bd23e-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="bd23e-158">輸出</span><span class="sxs-lookup"><span data-stu-id="bd23e-158">OUTPUTS</span></span>

### <span data-ttu-id="bd23e-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="bd23e-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bd23e-160">筆記</span><span class="sxs-lookup"><span data-stu-id="bd23e-160">NOTES</span></span>

## <span data-ttu-id="bd23e-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd23e-161">RELATED LINKS</span></span>

[<span data-ttu-id="bd23e-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd23e-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="bd23e-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd23e-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="bd23e-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd23e-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


