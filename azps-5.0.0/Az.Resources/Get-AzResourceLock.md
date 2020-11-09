---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286331"
---
# <span data-ttu-id="8d44d-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8d44d-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="8d44d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d44d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d44d-103">取得資源鎖。</span><span class="sxs-lookup"><span data-stu-id="8d44d-103">Gets a resource lock.</span></span>

## <span data-ttu-id="8d44d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d44d-104">SYNTAX</span></span>

### <span data-ttu-id="8d44d-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d44d-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d44d-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8d44d-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d44d-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="8d44d-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d44d-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8d44d-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d44d-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8d44d-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d44d-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="8d44d-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d44d-111">說明</span><span class="sxs-lookup"><span data-stu-id="8d44d-111">DESCRIPTION</span></span>
<span data-ttu-id="8d44d-112">**AzResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8d44d-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="8d44d-113">示例</span><span class="sxs-lookup"><span data-stu-id="8d44d-113">EXAMPLES</span></span>

### <span data-ttu-id="8d44d-114">範例1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="8d44d-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8d44d-115">這個命令會取得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8d44d-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="8d44d-116">範例2：取得資源群組層級或更新版本的鎖</span><span class="sxs-lookup"><span data-stu-id="8d44d-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="8d44d-117">這個命令會在資源群組或訂閱上取得資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8d44d-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="8d44d-118">參數</span><span class="sxs-lookup"><span data-stu-id="8d44d-118">PARAMETERS</span></span>

### <span data-ttu-id="8d44d-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8d44d-119">-ApiVersion</span></span>
<span data-ttu-id="8d44d-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8d44d-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8d44d-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="8d44d-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8d44d-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="8d44d-122">-AtScope</span></span>
<span data-ttu-id="8d44d-123">表示此 Cmdlet 會傳回指定範圍或其上方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="8d44d-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="8d44d-124">如果您沒有指定此參數，則 Cmdlet 會傳回範圍內、上方或下方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="8d44d-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="8d44d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d44d-125">-DefaultProfile</span></span>
<span data-ttu-id="8d44d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d44d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d44d-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="8d44d-127">-LockId</span></span>
<span data-ttu-id="8d44d-128">指定此 Cmdlet 取得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d44d-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8d44d-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="8d44d-129">-LockName</span></span>
<span data-ttu-id="8d44d-130">指定此 Cmdlet 取得的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="8d44d-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8d44d-131">-預先</span><span class="sxs-lookup"><span data-stu-id="8d44d-131">-Pre</span></span>
<span data-ttu-id="8d44d-132">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8d44d-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8d44d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d44d-133">-ResourceGroupName</span></span>
<span data-ttu-id="8d44d-134">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d44d-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="8d44d-135">這個 Cmdlet 會取得此資源群組的鎖定。</span><span class="sxs-lookup"><span data-stu-id="8d44d-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="8d44d-136">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="8d44d-136">-ResourceName</span></span>
<span data-ttu-id="8d44d-137">指定此鎖適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d44d-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="8d44d-138">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="8d44d-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8d44d-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8d44d-139">-ResourceType</span></span>
<span data-ttu-id="8d44d-140">指定此鎖適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8d44d-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="8d44d-141">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="8d44d-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8d44d-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="8d44d-142">-Scope</span></span>
<span data-ttu-id="8d44d-143">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="8d44d-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="8d44d-144">Cmdlet 會針對此範圍取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="8d44d-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="8d44d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d44d-145">CommonParameters</span></span>
<span data-ttu-id="8d44d-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d44d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d44d-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d44d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d44d-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8d44d-148">INPUTS</span></span>

### <span data-ttu-id="8d44d-149">System.object</span><span class="sxs-lookup"><span data-stu-id="8d44d-149">System.String</span></span>

## <span data-ttu-id="8d44d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="8d44d-150">OUTPUTS</span></span>

### <span data-ttu-id="8d44d-151">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="8d44d-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8d44d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="8d44d-152">NOTES</span></span>

## <span data-ttu-id="8d44d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d44d-153">RELATED LINKS</span></span>

[<span data-ttu-id="8d44d-154">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8d44d-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="8d44d-155">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8d44d-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="8d44d-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8d44d-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


