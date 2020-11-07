---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799745"
---
# <span data-ttu-id="f0303-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0303-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="f0303-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0303-102">SYNOPSIS</span></span>
<span data-ttu-id="f0303-103">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0303-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0303-104">SYNTAX</span></span>

### <span data-ttu-id="f0303-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0303-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0303-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0303-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0303-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0303-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0303-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0303-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0303-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0303-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0303-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0303-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0303-111">說明</span><span class="sxs-lookup"><span data-stu-id="f0303-111">DESCRIPTION</span></span>
<span data-ttu-id="f0303-112">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="f0303-113">示例</span><span class="sxs-lookup"><span data-stu-id="f0303-113">EXAMPLES</span></span>

### <span data-ttu-id="f0303-114">範例 1-依物件識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="f0303-115">移除物件 id 為 "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" 的服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="f0303-116">範例 2-依應用程式識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="f0303-117">移除應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76」的服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="f0303-118">範例 3-依 SPN 移除服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="f0303-119">移除服務主體名稱為 "MyServicePrincipal" 的服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="f0303-120">範例 4-依管道移除服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="f0303-121">取得 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 Cmdlet 的物件識別碼 '」和 Remove-AzureRmADServicePrincipal 管道的服務主體，以移除該服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="f0303-122">範例 5-依管道將應用程式移除服務主體</span><span class="sxs-lookup"><span data-stu-id="f0303-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="f0303-123">取得應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 以及 Remove-AzureRmADServicePrincipal Cmdlet 的管道的應用程式，以移除與該應用程式相關聯的服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="f0303-124">參數</span><span class="sxs-lookup"><span data-stu-id="f0303-124">PARAMETERS</span></span>

### <span data-ttu-id="f0303-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f0303-125">-ApplicationId</span></span>
<span data-ttu-id="f0303-126">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0303-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="f0303-127">-ApplicationObject</span></span>
<span data-ttu-id="f0303-128">要移除其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="f0303-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0303-129">-DefaultProfile</span></span>
<span data-ttu-id="f0303-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f0303-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0303-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f0303-131">-DisplayName</span></span>
<span data-ttu-id="f0303-132">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f0303-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-133">-Force</span><span class="sxs-lookup"><span data-stu-id="f0303-133">-Force</span></span>
<span data-ttu-id="f0303-134">如果沒有確認，請切換到刪除服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="f0303-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0303-135">-InputObject</span></span>
<span data-ttu-id="f0303-136">服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="f0303-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f0303-137">-ObjectId</span></span>
<span data-ttu-id="f0303-138">要刪除的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0303-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0303-139">-PassThru</span></span>
<span data-ttu-id="f0303-140">如果已指定，則傳回已刪除的服務主體。</span><span class="sxs-lookup"><span data-stu-id="f0303-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="f0303-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f0303-141">-ServicePrincipalName</span></span>
<span data-ttu-id="f0303-142">服務主要名稱。</span><span class="sxs-lookup"><span data-stu-id="f0303-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-143">-確認</span><span class="sxs-lookup"><span data-stu-id="f0303-143">-Confirm</span></span>
<span data-ttu-id="f0303-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0303-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0303-145">-WhatIf</span></span>
<span data-ttu-id="f0303-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0303-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0303-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0303-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0303-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0303-148">CommonParameters</span></span>
<span data-ttu-id="f0303-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0303-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0303-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0303-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0303-151">輸入</span><span class="sxs-lookup"><span data-stu-id="f0303-151">INPUTS</span></span>

### <span data-ttu-id="f0303-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="f0303-152">System.Guid</span></span>

### <span data-ttu-id="f0303-153">System.object</span><span class="sxs-lookup"><span data-stu-id="f0303-153">System.String</span></span>

### <span data-ttu-id="f0303-154">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0303-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="f0303-155">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f0303-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f0303-156">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f0303-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="f0303-157">參數： ApplicationObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f0303-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="f0303-158">輸出</span><span class="sxs-lookup"><span data-stu-id="f0303-158">OUTPUTS</span></span>

### <span data-ttu-id="f0303-159">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0303-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f0303-160">筆記</span><span class="sxs-lookup"><span data-stu-id="f0303-160">NOTES</span></span>
<span data-ttu-id="f0303-161">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="f0303-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f0303-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0303-162">RELATED LINKS</span></span>

[<span data-ttu-id="f0303-163">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0303-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f0303-164">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f0303-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="f0303-165">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f0303-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f0303-166">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f0303-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
