---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 3059e5611f843244f69cc48ae432ef070627d29d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407721"
---
# <span data-ttu-id="c06af-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c06af-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="c06af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c06af-102">SYNOPSIS</span></span>
<span data-ttu-id="c06af-103">刪除 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c06af-104">語法</span><span class="sxs-lookup"><span data-stu-id="c06af-104">SYNTAX</span></span>

### <span data-ttu-id="c06af-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c06af-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06af-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06af-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06af-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06af-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06af-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c06af-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c06af-109">描述</span><span class="sxs-lookup"><span data-stu-id="c06af-109">DESCRIPTION</span></span>
<span data-ttu-id="c06af-110">刪除 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c06af-111">例子</span><span class="sxs-lookup"><span data-stu-id="c06af-111">EXAMPLES</span></span>

### <span data-ttu-id="c06af-112">範例 1 - 根據物件識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="c06af-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="c06af-113">從租使用者移除具有物件識別碼 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="c06af-114">範例 2 - 根據應用程式識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="c06af-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="c06af-115">從租使用者移除應用程式識別碼為 'f9c5ea4f-28f0-401a-a491-491a037fa346'的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="c06af-116">範例 3 - 使用管道移除應用程式</span><span class="sxs-lookup"><span data-stu-id="c06af-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="c06af-117">使用物件識別碼 'b4cd1619-80b3-4cfb-9f8f-9f2333425738'及管道將應用程式從租使用者移除至 Remove-AzADApplication Cmdlet 的應用程式，來得到應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="c06af-118">參數</span><span class="sxs-lookup"><span data-stu-id="c06af-118">PARAMETERS</span></span>

### <span data-ttu-id="c06af-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c06af-119">-ApplicationId</span></span>
<span data-ttu-id="c06af-120">要移除的應用程式之應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c06af-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="c06af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06af-121">-DefaultProfile</span></span>
<span data-ttu-id="c06af-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c06af-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c06af-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c06af-123">-DisplayName</span></span>
<span data-ttu-id="c06af-124">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c06af-124">The display name of the application.</span></span>

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

### <span data-ttu-id="c06af-125">-強制</span><span class="sxs-lookup"><span data-stu-id="c06af-125">-Force</span></span>
<span data-ttu-id="c06af-126">切換以在未確認的情況下刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="c06af-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="c06af-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c06af-127">-InputObject</span></span>
<span data-ttu-id="c06af-128">代表要移除之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="c06af-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="c06af-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c06af-129">-ObjectId</span></span>
<span data-ttu-id="c06af-130">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c06af-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="c06af-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c06af-131">-PassThru</span></span>
<span data-ttu-id="c06af-132">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="c06af-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c06af-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c06af-133">-Confirm</span></span>
<span data-ttu-id="c06af-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c06af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06af-135">-WhatIf</span></span>
<span data-ttu-id="c06af-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c06af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06af-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c06af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06af-138">CommonParameters</span></span>
<span data-ttu-id="c06af-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c06af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06af-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c06af-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06af-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c06af-141">INPUTS</span></span>

### <span data-ttu-id="c06af-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c06af-142">System.String</span></span>

### <span data-ttu-id="c06af-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c06af-143">System.Guid</span></span>

### <span data-ttu-id="c06af-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c06af-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c06af-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c06af-145">OUTPUTS</span></span>

### <span data-ttu-id="c06af-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c06af-146">System.Boolean</span></span>

## <span data-ttu-id="c06af-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c06af-147">NOTES</span></span>
<span data-ttu-id="c06af-148">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="c06af-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c06af-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c06af-149">RELATED LINKS</span></span>

[<span data-ttu-id="c06af-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c06af-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="c06af-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c06af-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="c06af-152">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c06af-152">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

