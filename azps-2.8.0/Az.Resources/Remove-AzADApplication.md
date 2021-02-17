---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 7b66dff3f59e3ad186bfc559343aebf484ff2bc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413535"
---
# <span data-ttu-id="5a24a-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5a24a-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="5a24a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a24a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a24a-103">刪除 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a24a-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5a24a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a24a-104">SYNTAX</span></span>

### <span data-ttu-id="5a24a-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a24a-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a24a-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a24a-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a24a-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a24a-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a24a-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a24a-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a24a-109">描述</span><span class="sxs-lookup"><span data-stu-id="5a24a-109">DESCRIPTION</span></span>
<span data-ttu-id="5a24a-110">刪除 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a24a-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5a24a-111">例子</span><span class="sxs-lookup"><span data-stu-id="5a24a-111">EXAMPLES</span></span>

### <span data-ttu-id="5a24a-112">範例 1 - 根據物件識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="5a24a-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="5a24a-113">從租使用者移除具有物件識別碼 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a24a-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="5a24a-114">範例 2 - 根據應用程式識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="5a24a-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="5a24a-115">從租使用者移除應用程式識別碼為 'f9c5ea4f-28f0-401a-a491-491a037fa346'的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a24a-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="5a24a-116">範例 3 - 使用管道移除應用程式</span><span class="sxs-lookup"><span data-stu-id="5a24a-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="5a24a-117">使用物件識別碼 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'及管道將應用程式從租使用者移除至 Remove-AzADApplication Cmdlet 的應用程式，</span><span class="sxs-lookup"><span data-stu-id="5a24a-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="5a24a-118">參數</span><span class="sxs-lookup"><span data-stu-id="5a24a-118">PARAMETERS</span></span>

### <span data-ttu-id="5a24a-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5a24a-119">-ApplicationId</span></span>
<span data-ttu-id="5a24a-120">要移除的應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a24a-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="5a24a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a24a-121">-DefaultProfile</span></span>
<span data-ttu-id="5a24a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5a24a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a24a-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a24a-123">-DisplayName</span></span>
<span data-ttu-id="5a24a-124">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5a24a-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a24a-125">-強制</span><span class="sxs-lookup"><span data-stu-id="5a24a-125">-Force</span></span>
<span data-ttu-id="5a24a-126">切換以在未確認的情況下刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a24a-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="5a24a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a24a-127">-InputObject</span></span>
<span data-ttu-id="5a24a-128">代表要移除之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="5a24a-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a24a-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a24a-129">-ObjectId</span></span>
<span data-ttu-id="5a24a-130">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a24a-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a24a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a24a-131">-PassThru</span></span>
<span data-ttu-id="5a24a-132">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="5a24a-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5a24a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5a24a-133">-Confirm</span></span>
<span data-ttu-id="5a24a-134">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a24a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a24a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a24a-135">-WhatIf</span></span>
<span data-ttu-id="5a24a-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a24a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a24a-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a24a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a24a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a24a-138">CommonParameters</span></span>
<span data-ttu-id="5a24a-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a24a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a24a-140">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5a24a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a24a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5a24a-141">INPUTS</span></span>

### <span data-ttu-id="5a24a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5a24a-142">System.String</span></span>

### <span data-ttu-id="5a24a-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5a24a-143">System.Guid</span></span>

### <span data-ttu-id="5a24a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5a24a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="5a24a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5a24a-145">OUTPUTS</span></span>

### <span data-ttu-id="5a24a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a24a-146">System.Boolean</span></span>

## <span data-ttu-id="5a24a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5a24a-147">NOTES</span></span>
<span data-ttu-id="5a24a-148">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="5a24a-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5a24a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a24a-149">RELATED LINKS</span></span>

[<span data-ttu-id="5a24a-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5a24a-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="5a24a-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="5a24a-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="5a24a-152">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5a24a-152">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

