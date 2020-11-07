---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801141"
---
# <span data-ttu-id="0d0eb-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0d0eb-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="0d0eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0eb-103">取得資源鎖。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d0eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d0eb-104">SYNTAX</span></span>

### <span data-ttu-id="0d0eb-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0d0eb-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0d0eb-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0d0eb-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0d0eb-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0d0eb-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0d0eb-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d0eb-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="0d0eb-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d0eb-112">說明</span><span class="sxs-lookup"><span data-stu-id="0d0eb-112">DESCRIPTION</span></span>
<span data-ttu-id="0d0eb-113">**AzureRmResourceLock** Cmdlet 會取得 Azure 資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="0d0eb-114">示例</span><span class="sxs-lookup"><span data-stu-id="0d0eb-114">EXAMPLES</span></span>

### <span data-ttu-id="0d0eb-115">範例1：取得鎖定</span><span class="sxs-lookup"><span data-stu-id="0d0eb-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0d0eb-116">這個命令會取得名為 ContosoSiteLock 的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0d0eb-117">參數</span><span class="sxs-lookup"><span data-stu-id="0d0eb-117">PARAMETERS</span></span>

### <span data-ttu-id="0d0eb-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d0eb-118">-ApiVersion</span></span>
<span data-ttu-id="0d0eb-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d0eb-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d0eb-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="0d0eb-121">-AtScope</span></span>
<span data-ttu-id="0d0eb-122">表示此 Cmdlet 會傳回指定範圍或其上方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="0d0eb-123">如果您沒有指定此參數，則 Cmdlet 會傳回範圍內、上方或下方的所有鎖。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="0d0eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0eb-124">-DefaultProfile</span></span>
<span data-ttu-id="0d0eb-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0d0eb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d0eb-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0d0eb-126">-InformationAction</span></span>
<span data-ttu-id="0d0eb-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0d0eb-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d0eb-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d0eb-129">持續</span><span class="sxs-lookup"><span data-stu-id="0d0eb-129">Continue</span></span>
- <span data-ttu-id="0d0eb-130">理會</span><span class="sxs-lookup"><span data-stu-id="0d0eb-130">Ignore</span></span>
- <span data-ttu-id="0d0eb-131">看</span><span class="sxs-lookup"><span data-stu-id="0d0eb-131">Inquire</span></span>
- <span data-ttu-id="0d0eb-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d0eb-132">SilentlyContinue</span></span>
- <span data-ttu-id="0d0eb-133">停止</span><span class="sxs-lookup"><span data-stu-id="0d0eb-133">Stop</span></span>
- <span data-ttu-id="0d0eb-134">封存</span><span class="sxs-lookup"><span data-stu-id="0d0eb-134">Suspend</span></span>

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

### <span data-ttu-id="0d0eb-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d0eb-135">-InformationVariable</span></span>
<span data-ttu-id="0d0eb-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0d0eb-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="0d0eb-137">-LockId</span></span>
<span data-ttu-id="0d0eb-138">指定此 Cmdlet 取得之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d0eb-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="0d0eb-139">-LockName</span></span>
<span data-ttu-id="0d0eb-140">指定此 Cmdlet 取得的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d0eb-141">-預先</span><span class="sxs-lookup"><span data-stu-id="0d0eb-141">-Pre</span></span>
<span data-ttu-id="0d0eb-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d0eb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0eb-143">-ResourceGroupName</span></span>
<span data-ttu-id="0d0eb-144">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="0d0eb-145">這個 Cmdlet 會取得此資源群組的鎖定。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="0d0eb-146">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="0d0eb-146">-ResourceName</span></span>
<span data-ttu-id="0d0eb-147">指定此鎖適用之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="0d0eb-148">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0d0eb-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0d0eb-149">-ResourceType</span></span>
<span data-ttu-id="0d0eb-150">指定此鎖適用之資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="0d0eb-151">這個 Cmdlet 會取得此資源的鎖。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0d0eb-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="0d0eb-152">-Scope</span></span>
<span data-ttu-id="0d0eb-153">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0d0eb-154">Cmdlet 會針對此範圍取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="0d0eb-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0d0eb-155">-TenantLevel</span></span>
<span data-ttu-id="0d0eb-156">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0d0eb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0eb-157">CommonParameters</span></span>
<span data-ttu-id="0d0eb-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0eb-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d0eb-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0eb-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0d0eb-160">INPUTS</span></span>

## <span data-ttu-id="0d0eb-161">輸出</span><span class="sxs-lookup"><span data-stu-id="0d0eb-161">OUTPUTS</span></span>

## <span data-ttu-id="0d0eb-162">筆記</span><span class="sxs-lookup"><span data-stu-id="0d0eb-162">NOTES</span></span>

## <span data-ttu-id="0d0eb-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d0eb-163">RELATED LINKS</span></span>

[<span data-ttu-id="0d0eb-164">新-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0d0eb-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="0d0eb-165">移除-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0d0eb-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="0d0eb-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0d0eb-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


