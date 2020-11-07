---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797829"
---
# <span data-ttu-id="8cccd-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8cccd-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="8cccd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cccd-102">SYNOPSIS</span></span>
<span data-ttu-id="8cccd-103">取得資源鎖。</span><span class="sxs-lookup"><span data-stu-id="8cccd-103">Gets a resource lock.</span></span>

## <span data-ttu-id="8cccd-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cccd-104">SYNTAX</span></span>

### <span data-ttu-id="8cccd-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cccd-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cccd-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8cccd-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cccd-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="8cccd-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cccd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8cccd-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cccd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8cccd-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cccd-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8cccd-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cccd-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="8cccd-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cccd-112">說明</span><span class="sxs-lookup"><span data-stu-id="8cccd-112">DESCRIPTION</span></span>
<span data-ttu-id="8cccd-113">**AzResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8cccd-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="8cccd-114">示例</span><span class="sxs-lookup"><span data-stu-id="8cccd-114">EXAMPLES</span></span>

### <span data-ttu-id="8cccd-115">範例1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="8cccd-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8cccd-116">這個命令會取得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8cccd-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="8cccd-117">範例2：取得資源群組層級或更新版本的鎖</span><span class="sxs-lookup"><span data-stu-id="8cccd-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="8cccd-118">這個命令會在資源群組或訂閱上取得資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="8cccd-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="8cccd-119">參數</span><span class="sxs-lookup"><span data-stu-id="8cccd-119">PARAMETERS</span></span>

### <span data-ttu-id="8cccd-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cccd-120">-ApiVersion</span></span>
<span data-ttu-id="8cccd-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8cccd-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8cccd-122">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="8cccd-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8cccd-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="8cccd-123">-AtScope</span></span>
<span data-ttu-id="8cccd-124">表示此 Cmdlet 會傳回指定範圍或其上方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="8cccd-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="8cccd-125">如果您沒有指定此參數，則 Cmdlet 會傳回範圍內、上方或下方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="8cccd-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="8cccd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cccd-126">-DefaultProfile</span></span>
<span data-ttu-id="8cccd-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8cccd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cccd-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="8cccd-128">-LockId</span></span>
<span data-ttu-id="8cccd-129">指定此 Cmdlet 取得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cccd-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8cccd-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="8cccd-130">-LockName</span></span>
<span data-ttu-id="8cccd-131">指定此 Cmdlet 取得的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="8cccd-131">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8cccd-132">-預先</span><span class="sxs-lookup"><span data-stu-id="8cccd-132">-Pre</span></span>
<span data-ttu-id="8cccd-133">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8cccd-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8cccd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cccd-134">-ResourceGroupName</span></span>
<span data-ttu-id="8cccd-135">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cccd-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="8cccd-136">這個 Cmdlet 會取得此資源群組的鎖定。</span><span class="sxs-lookup"><span data-stu-id="8cccd-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="8cccd-137">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="8cccd-137">-ResourceName</span></span>
<span data-ttu-id="8cccd-138">指定此鎖適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cccd-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="8cccd-139">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="8cccd-139">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8cccd-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8cccd-140">-ResourceType</span></span>
<span data-ttu-id="8cccd-141">指定此鎖適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8cccd-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="8cccd-142">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="8cccd-142">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8cccd-143">-範圍</span><span class="sxs-lookup"><span data-stu-id="8cccd-143">-Scope</span></span>
<span data-ttu-id="8cccd-144">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="8cccd-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="8cccd-145">Cmdlet 會針對此範圍取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="8cccd-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="8cccd-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8cccd-146">-TenantLevel</span></span>
<span data-ttu-id="8cccd-147">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="8cccd-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8cccd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cccd-148">CommonParameters</span></span>
<span data-ttu-id="8cccd-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cccd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cccd-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8cccd-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cccd-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8cccd-151">INPUTS</span></span>

### <span data-ttu-id="8cccd-152">System.object</span><span class="sxs-lookup"><span data-stu-id="8cccd-152">System.String</span></span>

## <span data-ttu-id="8cccd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8cccd-153">OUTPUTS</span></span>

### <span data-ttu-id="8cccd-154">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="8cccd-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8cccd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8cccd-155">NOTES</span></span>

## <span data-ttu-id="8cccd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cccd-156">RELATED LINKS</span></span>

[<span data-ttu-id="8cccd-157">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8cccd-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="8cccd-158">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8cccd-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="8cccd-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="8cccd-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


