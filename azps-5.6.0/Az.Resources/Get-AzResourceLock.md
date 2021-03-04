---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 70c52508bbb152047d40d7556a41ad76e3ca2eac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904866"
---
# <span data-ttu-id="5bcda-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5bcda-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="5bcda-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5bcda-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcda-103">獲得資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-103">Gets a resource lock.</span></span>

## <span data-ttu-id="5bcda-104">語法</span><span class="sxs-lookup"><span data-stu-id="5bcda-104">SYNTAX</span></span>

### <span data-ttu-id="5bcda-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bcda-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcda-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="5bcda-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcda-107">ByS0ifiedScope</span><span class="sxs-lookup"><span data-stu-id="5bcda-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcda-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5bcda-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcda-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5bcda-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcda-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="5bcda-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bcda-111">描述</span><span class="sxs-lookup"><span data-stu-id="5bcda-111">DESCRIPTION</span></span>
<span data-ttu-id="5bcda-112">**Get-AzResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="5bcda-113">例子</span><span class="sxs-lookup"><span data-stu-id="5bcda-113">EXAMPLES</span></span>

### <span data-ttu-id="5bcda-114">範例 1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="5bcda-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5bcda-115">此命令會獲得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="5bcda-116">範例 2：取得資源群組層級或更高版本的鎖定</span><span class="sxs-lookup"><span data-stu-id="5bcda-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="5bcda-117">此命令會鎖定資源群組或訂閱的資源。</span><span class="sxs-lookup"><span data-stu-id="5bcda-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="5bcda-118">參數</span><span class="sxs-lookup"><span data-stu-id="5bcda-118">PARAMETERS</span></span>

### <span data-ttu-id="5bcda-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5bcda-119">-ApiVersion</span></span>
<span data-ttu-id="5bcda-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5bcda-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5bcda-121">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="5bcda-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5bcda-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="5bcda-122">-AtScope</span></span>
<span data-ttu-id="5bcda-123">表示此 Cmdlet 會返回指定範圍或上方的所有鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="5bcda-124">如果您未指定此參數，Cmdlet 會于範圍上方或下方，會返回所有鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="5bcda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcda-125">-DefaultProfile</span></span>
<span data-ttu-id="5bcda-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5bcda-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bcda-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="5bcda-127">-LockId</span></span>
<span data-ttu-id="5bcda-128">指定此 Cmdlet 所獲得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bcda-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5bcda-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="5bcda-129">-LockName</span></span>
<span data-ttu-id="5bcda-130">指定此 Cmdlet 所獲取的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcda-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcda-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bcda-131">-Pre</span></span>
<span data-ttu-id="5bcda-132">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="5bcda-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5bcda-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcda-133">-ResourceGroupName</span></span>
<span data-ttu-id="5bcda-134">指定鎖定所適用之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcda-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="5bcda-135">此 Cmdlet 會為此資源群組獲得鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="5bcda-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5bcda-136">-ResourceName</span></span>
<span data-ttu-id="5bcda-137">指定此鎖定所適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcda-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="5bcda-138">此 Cmdlet 會為此資源獲得鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="5bcda-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5bcda-139">-ResourceType</span></span>
<span data-ttu-id="5bcda-140">指定此鎖定所適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5bcda-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="5bcda-141">此 Cmdlet 會為此資源獲得鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="5bcda-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="5bcda-142">-Scope</span></span>
<span data-ttu-id="5bcda-143">指定鎖定所適用的範圍。</span><span class="sxs-lookup"><span data-stu-id="5bcda-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5bcda-144">Cmdlet 會為此範圍獲得鎖定。</span><span class="sxs-lookup"><span data-stu-id="5bcda-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="5bcda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcda-145">CommonParameters</span></span>
<span data-ttu-id="5bcda-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5bcda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcda-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bcda-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcda-148">輸入</span><span class="sxs-lookup"><span data-stu-id="5bcda-148">INPUTS</span></span>

### <span data-ttu-id="5bcda-149">System.String</span><span class="sxs-lookup"><span data-stu-id="5bcda-149">System.String</span></span>

## <span data-ttu-id="5bcda-150">輸出</span><span class="sxs-lookup"><span data-stu-id="5bcda-150">OUTPUTS</span></span>

### <span data-ttu-id="5bcda-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5bcda-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5bcda-152">筆記</span><span class="sxs-lookup"><span data-stu-id="5bcda-152">NOTES</span></span>

## <span data-ttu-id="5bcda-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bcda-153">RELATED LINKS</span></span>

[<span data-ttu-id="5bcda-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5bcda-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="5bcda-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5bcda-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="5bcda-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5bcda-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


