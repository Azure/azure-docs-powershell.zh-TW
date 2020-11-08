---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801874"
---
# <span data-ttu-id="25cff-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="25cff-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="25cff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25cff-102">SYNOPSIS</span></span>
<span data-ttu-id="25cff-103">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="25cff-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25cff-104">句法</span><span class="sxs-lookup"><span data-stu-id="25cff-104">SYNTAX</span></span>

### <span data-ttu-id="25cff-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="25cff-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cff-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cff-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cff-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cff-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cff-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cff-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25cff-109">說明</span><span class="sxs-lookup"><span data-stu-id="25cff-109">DESCRIPTION</span></span>
<span data-ttu-id="25cff-110">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="25cff-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="25cff-111">示例</span><span class="sxs-lookup"><span data-stu-id="25cff-111">EXAMPLES</span></span>

### <span data-ttu-id="25cff-112">範例 1-依物件識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="25cff-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="25cff-113">從租使用者移除物件 id 為 ' b4cd1619-80b3-4cfb-9f8f-9f2333425738」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="25cff-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="25cff-114">範例 2-依應用程式識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="25cff-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="25cff-115">從租使用者移除含應用程式識別碼 ' f9c5ea4f-28f0-401a-a491-491a037fa346」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="25cff-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="25cff-116">範例 3-透過管道移除應用程式</span><span class="sxs-lookup"><span data-stu-id="25cff-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="25cff-117">取得 b4cd1619-80b3-4cfb-9f8f-9f2333425738 Cmdlet 的物件識別碼 '」和 Remove-AzureRmADApplication 管道，以從租使用者中移除應用程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="25cff-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="25cff-118">參數</span><span class="sxs-lookup"><span data-stu-id="25cff-118">PARAMETERS</span></span>

### <span data-ttu-id="25cff-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="25cff-119">-ApplicationId</span></span>
<span data-ttu-id="25cff-120">要移除之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="25cff-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="25cff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cff-121">-DefaultProfile</span></span>
<span data-ttu-id="25cff-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="25cff-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25cff-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="25cff-123">-DisplayName</span></span>
<span data-ttu-id="25cff-124">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="25cff-124">The display name of the application.</span></span>

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

### <span data-ttu-id="25cff-125">-Force</span><span class="sxs-lookup"><span data-stu-id="25cff-125">-Force</span></span>
<span data-ttu-id="25cff-126">切換以刪除應用程式而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="25cff-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="25cff-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25cff-127">-InputObject</span></span>
<span data-ttu-id="25cff-128">代表要移除之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="25cff-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25cff-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="25cff-129">-ObjectId</span></span>
<span data-ttu-id="25cff-130">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="25cff-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25cff-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25cff-131">-PassThru</span></span>
<span data-ttu-id="25cff-132">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="25cff-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="25cff-133">-確認</span><span class="sxs-lookup"><span data-stu-id="25cff-133">-Confirm</span></span>
<span data-ttu-id="25cff-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25cff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cff-135">-WhatIf</span></span>
<span data-ttu-id="25cff-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25cff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25cff-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25cff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cff-138">CommonParameters</span></span>
<span data-ttu-id="25cff-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25cff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cff-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25cff-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cff-141">輸入</span><span class="sxs-lookup"><span data-stu-id="25cff-141">INPUTS</span></span>

### <span data-ttu-id="25cff-142">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="25cff-142">System.Guid</span></span>

### <span data-ttu-id="25cff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="25cff-143">System.String</span></span>

### <span data-ttu-id="25cff-144">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="25cff-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="25cff-145">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="25cff-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="25cff-146">輸出</span><span class="sxs-lookup"><span data-stu-id="25cff-146">OUTPUTS</span></span>

### <span data-ttu-id="25cff-147">System.object</span><span class="sxs-lookup"><span data-stu-id="25cff-147">System.Boolean</span></span>

## <span data-ttu-id="25cff-148">筆記</span><span class="sxs-lookup"><span data-stu-id="25cff-148">NOTES</span></span>
<span data-ttu-id="25cff-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="25cff-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="25cff-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="25cff-150">RELATED LINKS</span></span>

[<span data-ttu-id="25cff-151">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="25cff-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="25cff-152">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="25cff-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)



[<span data-ttu-id="25cff-153">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="25cff-153">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
