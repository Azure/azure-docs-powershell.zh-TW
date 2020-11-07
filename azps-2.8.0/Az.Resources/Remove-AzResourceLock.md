---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791161"
---
# <span data-ttu-id="94ad8-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="94ad8-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="94ad8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="94ad8-103">移除資源鎖。</span><span class="sxs-lookup"><span data-stu-id="94ad8-103">Removes a resource lock.</span></span>

## <span data-ttu-id="94ad8-104">句法</span><span class="sxs-lookup"><span data-stu-id="94ad8-104">SYNTAX</span></span>

### <span data-ttu-id="94ad8-105">ByLockId (預設) </span><span class="sxs-lookup"><span data-stu-id="94ad8-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ad8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94ad8-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ad8-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="94ad8-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ad8-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="94ad8-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ad8-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="94ad8-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ad8-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="94ad8-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94ad8-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="94ad8-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94ad8-112">說明</span><span class="sxs-lookup"><span data-stu-id="94ad8-112">DESCRIPTION</span></span>
<span data-ttu-id="94ad8-113">**AzResourceLock** Cmdlet 會移除 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ad8-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="94ad8-114">示例</span><span class="sxs-lookup"><span data-stu-id="94ad8-114">EXAMPLES</span></span>

### <span data-ttu-id="94ad8-115">範例1：移除鎖定</span><span class="sxs-lookup"><span data-stu-id="94ad8-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="94ad8-116">這個命令會移除名為 ContosoSiteLock 的鎖定。</span><span class="sxs-lookup"><span data-stu-id="94ad8-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="94ad8-117">參數</span><span class="sxs-lookup"><span data-stu-id="94ad8-117">PARAMETERS</span></span>

### <span data-ttu-id="94ad8-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94ad8-118">-ApiVersion</span></span>
<span data-ttu-id="94ad8-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="94ad8-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="94ad8-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="94ad8-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="94ad8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ad8-121">-DefaultProfile</span></span>
<span data-ttu-id="94ad8-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="94ad8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94ad8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="94ad8-123">-Force</span></span>
<span data-ttu-id="94ad8-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="94ad8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94ad8-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="94ad8-125">-LockId</span></span>
<span data-ttu-id="94ad8-126">指定此 Cmdlet 移除之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94ad8-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94ad8-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="94ad8-127">-LockName</span></span>
<span data-ttu-id="94ad8-128">指定此 Cmdlet 移除的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="94ad8-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94ad8-129">-預先</span><span class="sxs-lookup"><span data-stu-id="94ad8-129">-Pre</span></span>
<span data-ttu-id="94ad8-130">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="94ad8-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94ad8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ad8-131">-ResourceGroupName</span></span>
<span data-ttu-id="94ad8-132">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94ad8-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="94ad8-133">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="94ad8-133">-ResourceName</span></span>
<span data-ttu-id="94ad8-134">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="94ad8-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="94ad8-135">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="94ad8-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="94ad8-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="94ad8-136">-ResourceType</span></span>
<span data-ttu-id="94ad8-137">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="94ad8-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="94ad8-138">-範圍</span><span class="sxs-lookup"><span data-stu-id="94ad8-138">-Scope</span></span>
<span data-ttu-id="94ad8-139">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="94ad8-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="94ad8-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="94ad8-140">-TenantLevel</span></span>
<span data-ttu-id="94ad8-141">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="94ad8-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="94ad8-142">-確認</span><span class="sxs-lookup"><span data-stu-id="94ad8-142">-Confirm</span></span>
<span data-ttu-id="94ad8-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94ad8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ad8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ad8-144">-WhatIf</span></span>
<span data-ttu-id="94ad8-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94ad8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ad8-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94ad8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ad8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ad8-147">CommonParameters</span></span>
<span data-ttu-id="94ad8-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94ad8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ad8-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94ad8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ad8-150">輸入</span><span class="sxs-lookup"><span data-stu-id="94ad8-150">INPUTS</span></span>

### <span data-ttu-id="94ad8-151">System.object</span><span class="sxs-lookup"><span data-stu-id="94ad8-151">System.String</span></span>

## <span data-ttu-id="94ad8-152">輸出</span><span class="sxs-lookup"><span data-stu-id="94ad8-152">OUTPUTS</span></span>

### <span data-ttu-id="94ad8-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="94ad8-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="94ad8-154">筆記</span><span class="sxs-lookup"><span data-stu-id="94ad8-154">NOTES</span></span>

## <span data-ttu-id="94ad8-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="94ad8-155">RELATED LINKS</span></span>

[<span data-ttu-id="94ad8-156">AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="94ad8-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="94ad8-157">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="94ad8-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="94ad8-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="94ad8-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


