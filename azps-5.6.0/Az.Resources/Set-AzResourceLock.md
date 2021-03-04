---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: a633718402f7c06e583030c379544ff45a216fb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905834"
---
# <span data-ttu-id="8e41d-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8e41d-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="8e41d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e41d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e41d-103">修改資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8e41d-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="8e41d-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e41d-104">SYNTAX</span></span>

### <span data-ttu-id="8e41d-105">BySifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="8e41d-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e41d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e41d-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e41d-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8e41d-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e41d-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8e41d-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e41d-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8e41d-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e41d-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="8e41d-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e41d-111">描述</span><span class="sxs-lookup"><span data-stu-id="8e41d-111">DESCRIPTION</span></span>
<span data-ttu-id="8e41d-112">**Set-AzResourceLock** Cmdlet 會修改資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8e41d-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="8e41d-113">例子</span><span class="sxs-lookup"><span data-stu-id="8e41d-113">EXAMPLES</span></span>

### <span data-ttu-id="8e41d-114">範例 1：更新鎖定的筆記</span><span class="sxs-lookup"><span data-stu-id="8e41d-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8e41d-115">此命令會更新名為 ContosoSiteLock 之鎖定的附注。</span><span class="sxs-lookup"><span data-stu-id="8e41d-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="8e41d-116">參數</span><span class="sxs-lookup"><span data-stu-id="8e41d-116">PARAMETERS</span></span>

### <span data-ttu-id="8e41d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8e41d-117">-ApiVersion</span></span>
<span data-ttu-id="8e41d-118">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8e41d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8e41d-119">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="8e41d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8e41d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e41d-120">-DefaultProfile</span></span>
<span data-ttu-id="8e41d-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8e41d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e41d-122">-強制</span><span class="sxs-lookup"><span data-stu-id="8e41d-122">-Force</span></span>
<span data-ttu-id="8e41d-123">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8e41d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e41d-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="8e41d-124">-LockId</span></span>
<span data-ttu-id="8e41d-125">指定此 Cmdlet 修改之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e41d-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8e41d-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="8e41d-126">-LockLevel</span></span>
<span data-ttu-id="8e41d-127">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="8e41d-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="8e41d-128">目前，唯一有效的值是 CanNotDelete。</span><span class="sxs-lookup"><span data-stu-id="8e41d-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="8e41d-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="8e41d-129">-LockName</span></span>
<span data-ttu-id="8e41d-130">指定此 Cmdlet 修改的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="8e41d-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8e41d-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="8e41d-131">-LockNotes</span></span>
<span data-ttu-id="8e41d-132">指定鎖定的附注。</span><span class="sxs-lookup"><span data-stu-id="8e41d-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="8e41d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e41d-133">-Pre</span></span>
<span data-ttu-id="8e41d-134">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8e41d-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8e41d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e41d-135">-ResourceGroupName</span></span>
<span data-ttu-id="8e41d-136">指定鎖定所適用之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e41d-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="8e41d-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8e41d-137">-ResourceName</span></span>
<span data-ttu-id="8e41d-138">指定鎖定所適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e41d-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="8e41d-139">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="8e41d-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="8e41d-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8e41d-140">-ResourceType</span></span>
<span data-ttu-id="8e41d-141">指定鎖定所適用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8e41d-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="8e41d-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="8e41d-142">-Scope</span></span>
<span data-ttu-id="8e41d-143">指定鎖定所適用的範圍。</span><span class="sxs-lookup"><span data-stu-id="8e41d-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="8e41d-144">例如，若要指定資料庫，請使用下列格式：訂閱識別碼資源組名伺服器名稱資料庫名稱若要指定資源群組，請使用下列格式 `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` ： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名</span><span class="sxs-lookup"><span data-stu-id="8e41d-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="8e41d-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8e41d-145">-Confirm</span></span>
<span data-ttu-id="8e41d-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e41d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e41d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e41d-147">-WhatIf</span></span>
<span data-ttu-id="8e41d-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e41d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e41d-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e41d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e41d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e41d-150">CommonParameters</span></span>
<span data-ttu-id="8e41d-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e41d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e41d-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e41d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e41d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="8e41d-153">INPUTS</span></span>

### <span data-ttu-id="8e41d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8e41d-154">System.String</span></span>

### <span data-ttu-id="8e41d-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Lock.LockLevel</span><span class="sxs-lookup"><span data-stu-id="8e41d-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="8e41d-156">輸出</span><span class="sxs-lookup"><span data-stu-id="8e41d-156">OUTPUTS</span></span>

### <span data-ttu-id="8e41d-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8e41d-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8e41d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="8e41d-158">NOTES</span></span>

## <span data-ttu-id="8e41d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e41d-159">RELATED LINKS</span></span>

[<span data-ttu-id="8e41d-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8e41d-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="8e41d-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8e41d-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="8e41d-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8e41d-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


