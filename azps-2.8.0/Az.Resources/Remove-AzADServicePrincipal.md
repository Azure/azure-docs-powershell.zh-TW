---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 0fa6dde8584eb003bd479e9a73ec96176282d83c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792206"
---
# <span data-ttu-id="bb655-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bb655-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="bb655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb655-102">SYNOPSIS</span></span>
<span data-ttu-id="bb655-103">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="bb655-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb655-104">SYNTAX</span></span>

### <span data-ttu-id="bb655-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bb655-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb655-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb655-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb655-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb655-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb655-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb655-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb655-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb655-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb655-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb655-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb655-111">說明</span><span class="sxs-lookup"><span data-stu-id="bb655-111">DESCRIPTION</span></span>
<span data-ttu-id="bb655-112">刪除 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="bb655-113">示例</span><span class="sxs-lookup"><span data-stu-id="bb655-113">EXAMPLES</span></span>

### <span data-ttu-id="bb655-114">範例 1-依物件識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="bb655-115">移除物件 id 為 "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" 的服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="bb655-116">範例 2-依應用程式識別碼移除服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="bb655-117">移除應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76」的服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="bb655-118">範例 3-依 SPN 移除服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="bb655-119">移除服務主體名稱為 "MyServicePrincipal" 的服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="bb655-120">範例 4-依管道移除服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="bb655-121">取得 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 Cmdlet 的物件識別碼 '」和 Remove-AzADServicePrincipal 管道的服務主體，以移除該服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="bb655-122">範例 5-依管道將應用程式移除服務主體</span><span class="sxs-lookup"><span data-stu-id="bb655-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="bb655-123">取得應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 以及 Remove-AzADServicePrincipal Cmdlet 的管道的應用程式，以移除與該應用程式相關聯的服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="bb655-124">參數</span><span class="sxs-lookup"><span data-stu-id="bb655-124">PARAMETERS</span></span>

### <span data-ttu-id="bb655-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bb655-125">-ApplicationId</span></span>
<span data-ttu-id="bb655-126">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb655-126">The service principal application id.</span></span>

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

### <span data-ttu-id="bb655-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="bb655-127">-ApplicationObject</span></span>
<span data-ttu-id="bb655-128">要移除其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="bb655-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb655-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb655-129">-DefaultProfile</span></span>
<span data-ttu-id="bb655-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bb655-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb655-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bb655-131">-DisplayName</span></span>
<span data-ttu-id="bb655-132">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bb655-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="bb655-133">-Force</span><span class="sxs-lookup"><span data-stu-id="bb655-133">-Force</span></span>
<span data-ttu-id="bb655-134">如果沒有確認，請切換到刪除服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="bb655-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb655-135">-InputObject</span></span>
<span data-ttu-id="bb655-136">服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="bb655-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb655-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bb655-137">-ObjectId</span></span>
<span data-ttu-id="bb655-138">要刪除的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb655-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb655-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb655-139">-PassThru</span></span>
<span data-ttu-id="bb655-140">如果已指定，則傳回已刪除的服務主體。</span><span class="sxs-lookup"><span data-stu-id="bb655-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="bb655-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bb655-141">-ServicePrincipalName</span></span>
<span data-ttu-id="bb655-142">服務主要名稱。</span><span class="sxs-lookup"><span data-stu-id="bb655-142">The service principal name.</span></span>

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

### <span data-ttu-id="bb655-143">-確認</span><span class="sxs-lookup"><span data-stu-id="bb655-143">-Confirm</span></span>
<span data-ttu-id="bb655-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb655-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb655-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb655-145">-WhatIf</span></span>
<span data-ttu-id="bb655-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb655-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb655-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb655-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb655-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb655-148">CommonParameters</span></span>
<span data-ttu-id="bb655-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb655-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb655-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb655-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb655-151">輸入</span><span class="sxs-lookup"><span data-stu-id="bb655-151">INPUTS</span></span>

### <span data-ttu-id="bb655-152">System.object</span><span class="sxs-lookup"><span data-stu-id="bb655-152">System.String</span></span>

### <span data-ttu-id="bb655-153">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="bb655-153">System.Guid</span></span>

### <span data-ttu-id="bb655-154">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bb655-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="bb655-155">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bb655-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="bb655-156">輸出</span><span class="sxs-lookup"><span data-stu-id="bb655-156">OUTPUTS</span></span>

### <span data-ttu-id="bb655-157">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bb655-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="bb655-158">筆記</span><span class="sxs-lookup"><span data-stu-id="bb655-158">NOTES</span></span>
<span data-ttu-id="bb655-159">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="bb655-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bb655-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb655-160">RELATED LINKS</span></span>

[<span data-ttu-id="bb655-161">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bb655-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="bb655-162">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bb655-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="bb655-163">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bb655-163">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="bb655-164">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bb655-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="bb655-165">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bb655-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)