---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456403"
---
# <span data-ttu-id="1b580-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="1b580-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="1b580-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b580-102">SYNOPSIS</span></span>
<span data-ttu-id="1b580-103">建立資源鎖。</span><span class="sxs-lookup"><span data-stu-id="1b580-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b580-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b580-104">SYNTAX</span></span>

### <span data-ttu-id="1b580-105">在指定範圍內的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-105">A lock at the specified scope.</span></span> <span data-ttu-id="1b580-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="1b580-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b580-107">資源群組範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b580-108">資源群組資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b580-109">訂閱範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b580-110">訂閱資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b580-111">租使用者資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b580-112">鎖（依識別碼）。</span><span class="sxs-lookup"><span data-stu-id="1b580-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b580-113">說明</span><span class="sxs-lookup"><span data-stu-id="1b580-113">DESCRIPTION</span></span>
<span data-ttu-id="1b580-114">**新的-AzureRmResourceLock** Cmdlet 會建立資源鎖。</span><span class="sxs-lookup"><span data-stu-id="1b580-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="1b580-115">示例</span><span class="sxs-lookup"><span data-stu-id="1b580-115">EXAMPLES</span></span>

### <span data-ttu-id="1b580-116">範例1：在網站上建立資源鎖定</span><span class="sxs-lookup"><span data-stu-id="1b580-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="1b580-117">這個命令會在網站上建立資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="1b580-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="1b580-118">參數</span><span class="sxs-lookup"><span data-stu-id="1b580-118">PARAMETERS</span></span>

### <span data-ttu-id="1b580-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b580-119">-ApiVersion</span></span>
<span data-ttu-id="1b580-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1b580-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b580-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="1b580-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1b580-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1b580-122">-Force</span></span>
<span data-ttu-id="1b580-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1b580-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b580-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1b580-124">-InformationAction</span></span>
<span data-ttu-id="1b580-125">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1b580-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1b580-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1b580-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b580-127">持續</span><span class="sxs-lookup"><span data-stu-id="1b580-127">Continue</span></span>
- <span data-ttu-id="1b580-128">理會</span><span class="sxs-lookup"><span data-stu-id="1b580-128">Ignore</span></span>
- <span data-ttu-id="1b580-129">看</span><span class="sxs-lookup"><span data-stu-id="1b580-129">Inquire</span></span>
- <span data-ttu-id="1b580-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1b580-130">SilentlyContinue</span></span>
- <span data-ttu-id="1b580-131">停止</span><span class="sxs-lookup"><span data-stu-id="1b580-131">Stop</span></span>
- <span data-ttu-id="1b580-132">封存</span><span class="sxs-lookup"><span data-stu-id="1b580-132">Suspend</span></span>

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

### <span data-ttu-id="1b580-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1b580-133">-InformationVariable</span></span>
<span data-ttu-id="1b580-134">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1b580-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1b580-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="1b580-135">-LockId</span></span>
<span data-ttu-id="1b580-136">指定鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b580-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="1b580-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="1b580-137">-LockLevel</span></span>
<span data-ttu-id="1b580-138">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="1b580-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="1b580-139">目前唯一有效的值是 CanNotDelete。</span><span class="sxs-lookup"><span data-stu-id="1b580-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="1b580-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="1b580-140">-LockName</span></span>
<span data-ttu-id="1b580-141">指定鎖定的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b580-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="1b580-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="1b580-142">-LockNotes</span></span>
<span data-ttu-id="1b580-143">指定鎖定的備忘稿。</span><span class="sxs-lookup"><span data-stu-id="1b580-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="1b580-144">-預先</span><span class="sxs-lookup"><span data-stu-id="1b580-144">-Pre</span></span>
<span data-ttu-id="1b580-145">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1b580-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1b580-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b580-146">-ResourceGroupName</span></span>
<span data-ttu-id="1b580-147">指定鎖定適用之資源群組的名稱，或包含該鎖定所套用之資源群組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b580-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="1b580-148">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="1b580-148">-ResourceName</span></span>
<span data-ttu-id="1b580-149">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b580-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="1b580-150">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="1b580-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="1b580-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1b580-151">-ResourceType</span></span>
<span data-ttu-id="1b580-152">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1b580-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="1b580-153">-範圍</span><span class="sxs-lookup"><span data-stu-id="1b580-153">-Scope</span></span>
<span data-ttu-id="1b580-154">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="1b580-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="1b580-155">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="1b580-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="1b580-156">`/subscriptions/`訂閱識別碼 `/resourceGroups/` 資源組名稱 `/providers/Microsoft.Sql/servers/` 伺服器名稱 `/databases/` 資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="1b580-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="1b580-157">若要指定資源群組，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="1b580-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="1b580-158">`/subscriptions/`訂閱識別碼 `/resourceGroups/` 資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1b580-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="1b580-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1b580-159">-TenantLevel</span></span>
<span data-ttu-id="1b580-160">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="1b580-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="1b580-161">-確認</span><span class="sxs-lookup"><span data-stu-id="1b580-161">-Confirm</span></span>
<span data-ttu-id="1b580-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b580-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b580-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b580-163">-WhatIf</span></span>
<span data-ttu-id="1b580-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b580-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b580-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b580-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b580-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b580-166">-DefaultProfile</span></span>
<span data-ttu-id="1b580-167">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b580-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b580-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b580-168">CommonParameters</span></span>
<span data-ttu-id="1b580-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b580-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b580-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b580-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b580-171">輸入</span><span class="sxs-lookup"><span data-stu-id="1b580-171">INPUTS</span></span>

## <span data-ttu-id="1b580-172">輸出</span><span class="sxs-lookup"><span data-stu-id="1b580-172">OUTPUTS</span></span>

### <span data-ttu-id="1b580-173">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b580-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b580-174">筆記</span><span class="sxs-lookup"><span data-stu-id="1b580-174">NOTES</span></span>

## <span data-ttu-id="1b580-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b580-175">RELATED LINKS</span></span>

[<span data-ttu-id="1b580-176">AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="1b580-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="1b580-177">移除-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="1b580-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="1b580-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="1b580-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


