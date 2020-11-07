---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625069"
---
# <span data-ttu-id="69015-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="69015-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="69015-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69015-102">SYNOPSIS</span></span>
<span data-ttu-id="69015-103">修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="69015-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69015-104">句法</span><span class="sxs-lookup"><span data-stu-id="69015-104">SYNTAX</span></span>

### <span data-ttu-id="69015-105">在指定範圍內的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-105">A lock at the specified scope.</span></span> <span data-ttu-id="69015-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="69015-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69015-107">資源群組範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69015-108">資源群組資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69015-109">訂閱範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69015-110">訂閱資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69015-111">租使用者資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="69015-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69015-112">鎖（依識別碼）。</span><span class="sxs-lookup"><span data-stu-id="69015-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69015-113">說明</span><span class="sxs-lookup"><span data-stu-id="69015-113">DESCRIPTION</span></span>
<span data-ttu-id="69015-114">**AzureRmResourceLock** Cmdlet 會修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="69015-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="69015-115">示例</span><span class="sxs-lookup"><span data-stu-id="69015-115">EXAMPLES</span></span>

### <span data-ttu-id="69015-116">範例1：更新鎖定的筆記</span><span class="sxs-lookup"><span data-stu-id="69015-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="69015-117">這個命令會更新名為 ContosoSiteLock 之鎖定的筆記。</span><span class="sxs-lookup"><span data-stu-id="69015-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="69015-118">參數</span><span class="sxs-lookup"><span data-stu-id="69015-118">PARAMETERS</span></span>

### <span data-ttu-id="69015-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="69015-119">-ApiVersion</span></span>
<span data-ttu-id="69015-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="69015-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="69015-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="69015-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="69015-122">-Force</span><span class="sxs-lookup"><span data-stu-id="69015-122">-Force</span></span>
<span data-ttu-id="69015-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="69015-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69015-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="69015-124">-InformationAction</span></span>
<span data-ttu-id="69015-125">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="69015-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="69015-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="69015-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69015-127">持續</span><span class="sxs-lookup"><span data-stu-id="69015-127">Continue</span></span>
- <span data-ttu-id="69015-128">理會</span><span class="sxs-lookup"><span data-stu-id="69015-128">Ignore</span></span>
- <span data-ttu-id="69015-129">看</span><span class="sxs-lookup"><span data-stu-id="69015-129">Inquire</span></span>
- <span data-ttu-id="69015-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="69015-130">SilentlyContinue</span></span>
- <span data-ttu-id="69015-131">停止</span><span class="sxs-lookup"><span data-stu-id="69015-131">Stop</span></span>
- <span data-ttu-id="69015-132">封存</span><span class="sxs-lookup"><span data-stu-id="69015-132">Suspend</span></span>

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

### <span data-ttu-id="69015-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="69015-133">-InformationVariable</span></span>
<span data-ttu-id="69015-134">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="69015-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="69015-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="69015-135">-LockId</span></span>
<span data-ttu-id="69015-136">指定此 Cmdlet 所修改之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="69015-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="69015-137">-LockLevel</span></span>
<span data-ttu-id="69015-138">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="69015-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="69015-139">目前唯一有效的值是 CanNotDelete。</span><span class="sxs-lookup"><span data-stu-id="69015-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="69015-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="69015-140">-LockName</span></span>
<span data-ttu-id="69015-141">指定此 Cmdlet 修改的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="69015-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="69015-142">-LockNotes</span></span>
<span data-ttu-id="69015-143">指定鎖定的備忘稿。</span><span class="sxs-lookup"><span data-stu-id="69015-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="69015-144">-預先</span><span class="sxs-lookup"><span data-stu-id="69015-144">-Pre</span></span>
<span data-ttu-id="69015-145">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="69015-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="69015-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69015-146">-ResourceGroupName</span></span>
<span data-ttu-id="69015-147">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69015-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-148">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="69015-148">-ResourceName</span></span>
<span data-ttu-id="69015-149">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="69015-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="69015-150">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="69015-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="69015-151">伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="69015-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="69015-152">-ResourceType</span></span>
<span data-ttu-id="69015-153">指定要套用鎖定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="69015-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-154">-範圍</span><span class="sxs-lookup"><span data-stu-id="69015-154">-Scope</span></span>
<span data-ttu-id="69015-155">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="69015-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="69015-156">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="69015-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="69015-157">`/subscriptions/`訂閱識別碼 `/resourceGroups/` 資源組名稱 `/providers/Microsoft.Sql/servers/` 伺服器名稱 `/databases/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="69015-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="69015-158">若要指定資源群組，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="69015-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="69015-159">`/subscriptions/`訂閱識別碼 `/resourceGroups/` 資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="69015-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69015-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="69015-160">-TenantLevel</span></span>
<span data-ttu-id="69015-161">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="69015-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69015-162">-確認</span><span class="sxs-lookup"><span data-stu-id="69015-162">-Confirm</span></span>
<span data-ttu-id="69015-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69015-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69015-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69015-164">-WhatIf</span></span>
<span data-ttu-id="69015-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69015-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69015-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69015-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69015-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69015-167">-DefaultProfile</span></span>
<span data-ttu-id="69015-168">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69015-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69015-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69015-169">CommonParameters</span></span>
<span data-ttu-id="69015-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69015-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69015-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69015-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69015-172">輸入</span><span class="sxs-lookup"><span data-stu-id="69015-172">INPUTS</span></span>

## <span data-ttu-id="69015-173">輸出</span><span class="sxs-lookup"><span data-stu-id="69015-173">OUTPUTS</span></span>

### <span data-ttu-id="69015-174">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="69015-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="69015-175">筆記</span><span class="sxs-lookup"><span data-stu-id="69015-175">NOTES</span></span>

## <span data-ttu-id="69015-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="69015-176">RELATED LINKS</span></span>

[<span data-ttu-id="69015-177">AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="69015-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="69015-178">新-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="69015-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="69015-179">移除-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="69015-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


