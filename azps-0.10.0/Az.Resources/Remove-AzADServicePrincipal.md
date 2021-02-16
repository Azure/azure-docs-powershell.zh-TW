---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: bd58a044db49cdd0cedf2872e97e64662a49372c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398218"
---
# <span data-ttu-id="97a5e-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a5e-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="97a5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="97a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="97a5e-103">刪除 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="97a5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="97a5e-104">SYNTAX</span></span>

### <span data-ttu-id="97a5e-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="97a5e-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5e-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a5e-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5e-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a5e-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5e-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a5e-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a5e-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5e-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a5e-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a5e-111">描述</span><span class="sxs-lookup"><span data-stu-id="97a5e-111">DESCRIPTION</span></span>
<span data-ttu-id="97a5e-112">刪除 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="97a5e-113">例子</span><span class="sxs-lookup"><span data-stu-id="97a5e-113">EXAMPLES</span></span>

### <span data-ttu-id="97a5e-114">範例 1 - 根據物件識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="97a5e-115">移除具有物件識別碼 '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'的服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="97a5e-116">範例 2 - 根據應用程式識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="97a5e-117">移除具有應用程式識別碼 '9263469e-d328-4321-8646-3e3e75d20e76'的服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="97a5e-118">範例 3 - 根據 SPN 移除服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="97a5e-119">移除服務主體名稱為 "MyServicePrincipal" 的服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="97a5e-120">範例 4 - 使用管道移除服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="97a5e-121">使用物件識別碼 '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' 和服務管道到 Remove-AzADServicePrincipal Cmdlet 以移除該服務主體來獲得服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="97a5e-122">範例 5 - 使用管道處理應用程式來移除服務主體</span><span class="sxs-lookup"><span data-stu-id="97a5e-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="97a5e-123">使用應用程式識別碼為 '9263469e-d328-4321-8646-3e3e75d20e76' 的應用程式，以及管道到 Remove-AzADServicePrincipal Cmdlet 以移除與該應用程式相關聯的服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="97a5e-124">參數</span><span class="sxs-lookup"><span data-stu-id="97a5e-124">PARAMETERS</span></span>

### <span data-ttu-id="97a5e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="97a5e-125">-ApplicationId</span></span>
<span data-ttu-id="97a5e-126">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="97a5e-126">The service principal application id.</span></span>

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

### <span data-ttu-id="97a5e-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="97a5e-127">-ApplicationObject</span></span>
<span data-ttu-id="97a5e-128">正在移除其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="97a5e-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="97a5e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a5e-129">-DefaultProfile</span></span>
<span data-ttu-id="97a5e-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="97a5e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97a5e-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="97a5e-131">-DisplayName</span></span>
<span data-ttu-id="97a5e-132">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="97a5e-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="97a5e-133">-強制</span><span class="sxs-lookup"><span data-stu-id="97a5e-133">-Force</span></span>
<span data-ttu-id="97a5e-134">切換至刪除服務主體而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="97a5e-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="97a5e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97a5e-135">-InputObject</span></span>
<span data-ttu-id="97a5e-136">服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="97a5e-136">The service principal object.</span></span>

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

### <span data-ttu-id="97a5e-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="97a5e-137">-ObjectId</span></span>
<span data-ttu-id="97a5e-138">要刪除的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="97a5e-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="97a5e-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97a5e-139">-PassThru</span></span>
<span data-ttu-id="97a5e-140">如果指定，會返回已刪除的服務主體。</span><span class="sxs-lookup"><span data-stu-id="97a5e-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="97a5e-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="97a5e-141">-ServicePrincipalName</span></span>
<span data-ttu-id="97a5e-142">服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="97a5e-142">The service principal name.</span></span>

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

### <span data-ttu-id="97a5e-143">-確認</span><span class="sxs-lookup"><span data-stu-id="97a5e-143">-Confirm</span></span>
<span data-ttu-id="97a5e-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="97a5e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a5e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a5e-145">-WhatIf</span></span>
<span data-ttu-id="97a5e-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97a5e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a5e-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97a5e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a5e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a5e-148">CommonParameters</span></span>
<span data-ttu-id="97a5e-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="97a5e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a5e-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="97a5e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a5e-151">輸入</span><span class="sxs-lookup"><span data-stu-id="97a5e-151">INPUTS</span></span>

### <span data-ttu-id="97a5e-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="97a5e-152">System.Guid</span></span>

### <span data-ttu-id="97a5e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="97a5e-153">System.String</span></span>

### <span data-ttu-id="97a5e-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a5e-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="97a5e-155">參數：InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="97a5e-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="97a5e-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="97a5e-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="97a5e-157">參數：ApplicationObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="97a5e-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="97a5e-158">輸出</span><span class="sxs-lookup"><span data-stu-id="97a5e-158">OUTPUTS</span></span>

### <span data-ttu-id="97a5e-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a5e-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="97a5e-160">筆記</span><span class="sxs-lookup"><span data-stu-id="97a5e-160">NOTES</span></span>
<span data-ttu-id="97a5e-161">關鍵字：azure、Az、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="97a5e-161">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="97a5e-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="97a5e-162">RELATED LINKS</span></span>

[<span data-ttu-id="97a5e-163">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a5e-163">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="97a5e-164">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a5e-164">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


[<span data-ttu-id="97a5e-165">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="97a5e-165">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="97a5e-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="97a5e-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
