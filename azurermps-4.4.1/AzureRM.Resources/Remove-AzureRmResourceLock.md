---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452363"
---
# <span data-ttu-id="68d28-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="68d28-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="68d28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68d28-102">SYNOPSIS</span></span>
<span data-ttu-id="68d28-103">移除資源鎖。</span><span class="sxs-lookup"><span data-stu-id="68d28-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68d28-104">句法</span><span class="sxs-lookup"><span data-stu-id="68d28-104">SYNTAX</span></span>

### <span data-ttu-id="68d28-105">[依 Id] (的鎖。預設) </span><span class="sxs-lookup"><span data-stu-id="68d28-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d28-106">資源群組範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d28-107">資源群組資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d28-108">在指定範圍內的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d28-109">訂閱範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68d28-110">訂閱資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68d28-111">租使用者資源範圍的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68d28-112">說明</span><span class="sxs-lookup"><span data-stu-id="68d28-112">DESCRIPTION</span></span>
<span data-ttu-id="68d28-113">**AzureRmResourceLock** Cmdlet 會移除 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="68d28-114">示例</span><span class="sxs-lookup"><span data-stu-id="68d28-114">EXAMPLES</span></span>

### <span data-ttu-id="68d28-115">範例1：移除鎖定</span><span class="sxs-lookup"><span data-stu-id="68d28-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="68d28-116">這個命令會移除名為 ContosoSiteLock 的鎖定。</span><span class="sxs-lookup"><span data-stu-id="68d28-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="68d28-117">參數</span><span class="sxs-lookup"><span data-stu-id="68d28-117">PARAMETERS</span></span>

### <span data-ttu-id="68d28-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68d28-118">-ApiVersion</span></span>
<span data-ttu-id="68d28-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="68d28-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="68d28-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="68d28-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="68d28-121">-Force</span><span class="sxs-lookup"><span data-stu-id="68d28-121">-Force</span></span>
<span data-ttu-id="68d28-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="68d28-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68d28-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="68d28-123">-InformationAction</span></span>
<span data-ttu-id="68d28-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="68d28-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="68d28-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="68d28-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68d28-126">持續</span><span class="sxs-lookup"><span data-stu-id="68d28-126">Continue</span></span>
- <span data-ttu-id="68d28-127">理會</span><span class="sxs-lookup"><span data-stu-id="68d28-127">Ignore</span></span>
- <span data-ttu-id="68d28-128">看</span><span class="sxs-lookup"><span data-stu-id="68d28-128">Inquire</span></span>
- <span data-ttu-id="68d28-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="68d28-129">SilentlyContinue</span></span>
- <span data-ttu-id="68d28-130">停止</span><span class="sxs-lookup"><span data-stu-id="68d28-130">Stop</span></span>
- <span data-ttu-id="68d28-131">封存</span><span class="sxs-lookup"><span data-stu-id="68d28-131">Suspend</span></span>

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

### <span data-ttu-id="68d28-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="68d28-132">-InformationVariable</span></span>
<span data-ttu-id="68d28-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="68d28-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="68d28-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="68d28-134">-LockId</span></span>
<span data-ttu-id="68d28-135">指定此 Cmdlet 移除之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="68d28-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68d28-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="68d28-136">-LockName</span></span>
<span data-ttu-id="68d28-137">指定此 Cmdlet 移除的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="68d28-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68d28-138">-預先</span><span class="sxs-lookup"><span data-stu-id="68d28-138">-Pre</span></span>
<span data-ttu-id="68d28-139">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="68d28-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68d28-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d28-140">-ResourceGroupName</span></span>
<span data-ttu-id="68d28-141">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68d28-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="68d28-142">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="68d28-142">-ResourceName</span></span>
<span data-ttu-id="68d28-143">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="68d28-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="68d28-144">例如，若要指定資料庫，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="68d28-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="68d28-145">伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="68d28-145">Server`/`Database</span></span>

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

### <span data-ttu-id="68d28-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="68d28-146">-ResourceType</span></span>
<span data-ttu-id="68d28-147">指定要為其套用鎖定之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="68d28-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="68d28-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="68d28-148">-Scope</span></span>
<span data-ttu-id="68d28-149">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="68d28-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="68d28-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="68d28-150">-TenantLevel</span></span>
<span data-ttu-id="68d28-151">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="68d28-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="68d28-152">-確認</span><span class="sxs-lookup"><span data-stu-id="68d28-152">-Confirm</span></span>
<span data-ttu-id="68d28-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68d28-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d28-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d28-154">-WhatIf</span></span>
<span data-ttu-id="68d28-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68d28-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d28-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68d28-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d28-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d28-157">-DefaultProfile</span></span>
<span data-ttu-id="68d28-158">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68d28-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68d28-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d28-159">CommonParameters</span></span>
<span data-ttu-id="68d28-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68d28-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d28-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68d28-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d28-162">輸入</span><span class="sxs-lookup"><span data-stu-id="68d28-162">INPUTS</span></span>

## <span data-ttu-id="68d28-163">輸出</span><span class="sxs-lookup"><span data-stu-id="68d28-163">OUTPUTS</span></span>

### <span data-ttu-id="68d28-164">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="68d28-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="68d28-165">筆記</span><span class="sxs-lookup"><span data-stu-id="68d28-165">NOTES</span></span>

## <span data-ttu-id="68d28-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="68d28-166">RELATED LINKS</span></span>

[<span data-ttu-id="68d28-167">AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="68d28-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="68d28-168">新-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="68d28-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="68d28-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="68d28-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


