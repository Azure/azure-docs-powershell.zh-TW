---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: e774b333703714246de852d3f72ba704d7122b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795306"
---
# <span data-ttu-id="0a90e-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0a90e-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="0a90e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a90e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a90e-103">取得資源鎖。</span><span class="sxs-lookup"><span data-stu-id="0a90e-103">Gets a resource lock.</span></span>

## <span data-ttu-id="0a90e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a90e-104">SYNTAX</span></span>

### <span data-ttu-id="0a90e-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a90e-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0a90e-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0a90e-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0a90e-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0a90e-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0a90e-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a90e-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="0a90e-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a90e-112">說明</span><span class="sxs-lookup"><span data-stu-id="0a90e-112">DESCRIPTION</span></span>
<span data-ttu-id="0a90e-113">**AzResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="0a90e-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="0a90e-114">示例</span><span class="sxs-lookup"><span data-stu-id="0a90e-114">EXAMPLES</span></span>

### <span data-ttu-id="0a90e-115">範例1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="0a90e-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0a90e-116">這個命令會取得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="0a90e-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0a90e-117">參數</span><span class="sxs-lookup"><span data-stu-id="0a90e-117">PARAMETERS</span></span>

### <span data-ttu-id="0a90e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0a90e-118">-ApiVersion</span></span>
<span data-ttu-id="0a90e-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0a90e-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0a90e-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="0a90e-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0a90e-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="0a90e-121">-AtScope</span></span>
<span data-ttu-id="0a90e-122">表示此 Cmdlet 會傳回指定範圍或其上方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="0a90e-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="0a90e-123">如果您沒有指定此參數，則 Cmdlet 會傳回範圍內、上方或下方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="0a90e-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="0a90e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a90e-124">-DefaultProfile</span></span>
<span data-ttu-id="0a90e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a90e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a90e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0a90e-126">-InformationAction</span></span>
<span data-ttu-id="0a90e-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0a90e-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0a90e-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0a90e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a90e-129">持續</span><span class="sxs-lookup"><span data-stu-id="0a90e-129">Continue</span></span>
- <span data-ttu-id="0a90e-130">理會</span><span class="sxs-lookup"><span data-stu-id="0a90e-130">Ignore</span></span>
- <span data-ttu-id="0a90e-131">看</span><span class="sxs-lookup"><span data-stu-id="0a90e-131">Inquire</span></span>
- <span data-ttu-id="0a90e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a90e-132">SilentlyContinue</span></span>
- <span data-ttu-id="0a90e-133">停止</span><span class="sxs-lookup"><span data-stu-id="0a90e-133">Stop</span></span>
- <span data-ttu-id="0a90e-134">封存</span><span class="sxs-lookup"><span data-stu-id="0a90e-134">Suspend</span></span>

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

### <span data-ttu-id="0a90e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a90e-135">-InformationVariable</span></span>
<span data-ttu-id="0a90e-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0a90e-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a90e-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="0a90e-137">-LockId</span></span>
<span data-ttu-id="0a90e-138">指定此 Cmdlet 取得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a90e-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a90e-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="0a90e-139">-LockName</span></span>
<span data-ttu-id="0a90e-140">指定此 Cmdlet 取得的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="0a90e-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a90e-141">-預先</span><span class="sxs-lookup"><span data-stu-id="0a90e-141">-Pre</span></span>
<span data-ttu-id="0a90e-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0a90e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0a90e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a90e-143">-ResourceGroupName</span></span>
<span data-ttu-id="0a90e-144">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a90e-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="0a90e-145">這個 Cmdlet 會取得此資源群組的鎖定。</span><span class="sxs-lookup"><span data-stu-id="0a90e-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="0a90e-146">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="0a90e-146">-ResourceName</span></span>
<span data-ttu-id="0a90e-147">指定此鎖適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a90e-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="0a90e-148">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="0a90e-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0a90e-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0a90e-149">-ResourceType</span></span>
<span data-ttu-id="0a90e-150">指定此鎖適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0a90e-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="0a90e-151">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="0a90e-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0a90e-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="0a90e-152">-Scope</span></span>
<span data-ttu-id="0a90e-153">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="0a90e-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0a90e-154">Cmdlet 會針對此範圍取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="0a90e-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="0a90e-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0a90e-155">-TenantLevel</span></span>
<span data-ttu-id="0a90e-156">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="0a90e-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0a90e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a90e-157">CommonParameters</span></span>
<span data-ttu-id="0a90e-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a90e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a90e-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a90e-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a90e-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0a90e-160">INPUTS</span></span>

## <span data-ttu-id="0a90e-161">輸出</span><span class="sxs-lookup"><span data-stu-id="0a90e-161">OUTPUTS</span></span>

## <span data-ttu-id="0a90e-162">筆記</span><span class="sxs-lookup"><span data-stu-id="0a90e-162">NOTES</span></span>

## <span data-ttu-id="0a90e-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a90e-163">RELATED LINKS</span></span>

[<span data-ttu-id="0a90e-164">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0a90e-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="0a90e-165">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0a90e-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="0a90e-166">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0a90e-166">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


