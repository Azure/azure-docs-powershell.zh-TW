---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c719eee4800b404d691d478a989fdfdb3e7be09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455063"
---
# <span data-ttu-id="bc7f1-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc7f1-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="bc7f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7f1-103">移除資源鎖。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc7f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc7f1-104">SYNTAX</span></span>

### <span data-ttu-id="bc7f1-105">ByLockId (預設) </span><span class="sxs-lookup"><span data-stu-id="bc7f1-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc7f1-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bc7f1-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bc7f1-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bc7f1-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bc7f1-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7f1-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc7f1-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc7f1-112">說明</span><span class="sxs-lookup"><span data-stu-id="bc7f1-112">DESCRIPTION</span></span>
<span data-ttu-id="bc7f1-113">**AzureRmResourceLock** Cmdlet 會移除 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="bc7f1-114">示例</span><span class="sxs-lookup"><span data-stu-id="bc7f1-114">EXAMPLES</span></span>

### <span data-ttu-id="bc7f1-115">範例1：移除鎖定</span><span class="sxs-lookup"><span data-stu-id="bc7f1-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="bc7f1-116">這個命令會移除名為 ContosoSiteLock 的鎖定。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bc7f1-117">參數</span><span class="sxs-lookup"><span data-stu-id="bc7f1-117">PARAMETERS</span></span>

### <span data-ttu-id="bc7f1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc7f1-118">-ApiVersion</span></span>
<span data-ttu-id="bc7f1-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bc7f1-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bc7f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7f1-121">-DefaultProfile</span></span>
<span data-ttu-id="bc7f1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bc7f1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc7f1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bc7f1-123">-Force</span></span>
<span data-ttu-id="bc7f1-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc7f1-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bc7f1-125">-InformationAction</span></span>
<span data-ttu-id="bc7f1-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bc7f1-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bc7f1-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc7f1-128">持續</span><span class="sxs-lookup"><span data-stu-id="bc7f1-128">Continue</span></span>
- <span data-ttu-id="bc7f1-129">理會</span><span class="sxs-lookup"><span data-stu-id="bc7f1-129">Ignore</span></span>
- <span data-ttu-id="bc7f1-130">看</span><span class="sxs-lookup"><span data-stu-id="bc7f1-130">Inquire</span></span>
- <span data-ttu-id="bc7f1-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc7f1-131">SilentlyContinue</span></span>
- <span data-ttu-id="bc7f1-132">停止</span><span class="sxs-lookup"><span data-stu-id="bc7f1-132">Stop</span></span>
- <span data-ttu-id="bc7f1-133">封存</span><span class="sxs-lookup"><span data-stu-id="bc7f1-133">Suspend</span></span>

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

### <span data-ttu-id="bc7f1-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc7f1-134">-InformationVariable</span></span>
<span data-ttu-id="bc7f1-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc7f1-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="bc7f1-136">-LockId</span></span>
<span data-ttu-id="bc7f1-137">指定此 Cmdlet 移除之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc7f1-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="bc7f1-138">-LockName</span></span>
<span data-ttu-id="bc7f1-139">指定此 Cmdlet 移除的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc7f1-140">-預先</span><span class="sxs-lookup"><span data-stu-id="bc7f1-140">-Pre</span></span>
<span data-ttu-id="bc7f1-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bc7f1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc7f1-142">-ResourceGroupName</span></span>
<span data-ttu-id="bc7f1-143">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="bc7f1-144">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="bc7f1-144">-ResourceName</span></span>
<span data-ttu-id="bc7f1-145">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bc7f1-146">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="bc7f1-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="bc7f1-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bc7f1-147">-ResourceType</span></span>
<span data-ttu-id="bc7f1-148">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="bc7f1-149">-範圍</span><span class="sxs-lookup"><span data-stu-id="bc7f1-149">-Scope</span></span>
<span data-ttu-id="bc7f1-150">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="bc7f1-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc7f1-151">-TenantLevel</span></span>
<span data-ttu-id="bc7f1-152">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="bc7f1-153">-確認</span><span class="sxs-lookup"><span data-stu-id="bc7f1-153">-Confirm</span></span>
<span data-ttu-id="bc7f1-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc7f1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7f1-155">-WhatIf</span></span>
<span data-ttu-id="bc7f1-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc7f1-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc7f1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7f1-158">CommonParameters</span></span>
<span data-ttu-id="bc7f1-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7f1-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc7f1-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7f1-161">輸入</span><span class="sxs-lookup"><span data-stu-id="bc7f1-161">INPUTS</span></span>

## <span data-ttu-id="bc7f1-162">輸出</span><span class="sxs-lookup"><span data-stu-id="bc7f1-162">OUTPUTS</span></span>

## <span data-ttu-id="bc7f1-163">筆記</span><span class="sxs-lookup"><span data-stu-id="bc7f1-163">NOTES</span></span>

## <span data-ttu-id="bc7f1-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc7f1-164">RELATED LINKS</span></span>

[<span data-ttu-id="bc7f1-165">AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc7f1-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="bc7f1-166">新-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc7f1-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="bc7f1-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bc7f1-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


