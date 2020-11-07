---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792238"
---
# <span data-ttu-id="1580e-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1580e-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="1580e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1580e-102">SYNOPSIS</span></span>
<span data-ttu-id="1580e-103">取得資源鎖。</span><span class="sxs-lookup"><span data-stu-id="1580e-103">Gets a resource lock.</span></span>

## <span data-ttu-id="1580e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1580e-104">SYNTAX</span></span>

### <span data-ttu-id="1580e-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1580e-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1580e-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="1580e-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1580e-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="1580e-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1580e-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="1580e-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1580e-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="1580e-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1580e-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="1580e-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1580e-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="1580e-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1580e-112">說明</span><span class="sxs-lookup"><span data-stu-id="1580e-112">DESCRIPTION</span></span>
<span data-ttu-id="1580e-113">**AzResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="1580e-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="1580e-114">示例</span><span class="sxs-lookup"><span data-stu-id="1580e-114">EXAMPLES</span></span>

### <span data-ttu-id="1580e-115">範例1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="1580e-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1580e-116">這個命令會取得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="1580e-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="1580e-117">參數</span><span class="sxs-lookup"><span data-stu-id="1580e-117">PARAMETERS</span></span>

### <span data-ttu-id="1580e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1580e-118">-ApiVersion</span></span>
<span data-ttu-id="1580e-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1580e-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1580e-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="1580e-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1580e-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="1580e-121">-AtScope</span></span>
<span data-ttu-id="1580e-122">表示此 Cmdlet 會傳回指定範圍或其上方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="1580e-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="1580e-123">如果您沒有指定此參數，則 Cmdlet 會傳回範圍內、上方或下方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="1580e-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="1580e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1580e-124">-DefaultProfile</span></span>
<span data-ttu-id="1580e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1580e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1580e-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="1580e-126">-LockId</span></span>
<span data-ttu-id="1580e-127">指定此 Cmdlet 取得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1580e-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1580e-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="1580e-128">-LockName</span></span>
<span data-ttu-id="1580e-129">指定此 Cmdlet 取得的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="1580e-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1580e-130">-預先</span><span class="sxs-lookup"><span data-stu-id="1580e-130">-Pre</span></span>
<span data-ttu-id="1580e-131">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1580e-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1580e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1580e-132">-ResourceGroupName</span></span>
<span data-ttu-id="1580e-133">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1580e-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="1580e-134">這個 Cmdlet 會取得此資源群組的鎖定。</span><span class="sxs-lookup"><span data-stu-id="1580e-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="1580e-135">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="1580e-135">-ResourceName</span></span>
<span data-ttu-id="1580e-136">指定此鎖適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1580e-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="1580e-137">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="1580e-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="1580e-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1580e-138">-ResourceType</span></span>
<span data-ttu-id="1580e-139">指定此鎖適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1580e-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="1580e-140">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="1580e-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="1580e-141">-範圍</span><span class="sxs-lookup"><span data-stu-id="1580e-141">-Scope</span></span>
<span data-ttu-id="1580e-142">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="1580e-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="1580e-143">Cmdlet 會針對此範圍取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="1580e-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="1580e-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1580e-144">-TenantLevel</span></span>
<span data-ttu-id="1580e-145">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="1580e-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="1580e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1580e-146">CommonParameters</span></span>
<span data-ttu-id="1580e-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1580e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1580e-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1580e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1580e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1580e-149">INPUTS</span></span>

### <span data-ttu-id="1580e-150">System.object</span><span class="sxs-lookup"><span data-stu-id="1580e-150">System.String</span></span>

## <span data-ttu-id="1580e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="1580e-151">OUTPUTS</span></span>

### <span data-ttu-id="1580e-152">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="1580e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1580e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="1580e-153">NOTES</span></span>

## <span data-ttu-id="1580e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="1580e-154">RELATED LINKS</span></span>

[<span data-ttu-id="1580e-155">新-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1580e-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="1580e-156">移除-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1580e-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="1580e-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="1580e-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


