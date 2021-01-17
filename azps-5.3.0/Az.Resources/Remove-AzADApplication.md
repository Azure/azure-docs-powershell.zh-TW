---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435420"
---
# <span data-ttu-id="026d3-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="026d3-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="026d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="026d3-102">SYNOPSIS</span></span>
<span data-ttu-id="026d3-103">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="026d3-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="026d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="026d3-104">SYNTAX</span></span>

### <span data-ttu-id="026d3-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="026d3-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="026d3-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="026d3-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="026d3-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="026d3-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="026d3-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="026d3-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="026d3-109">說明</span><span class="sxs-lookup"><span data-stu-id="026d3-109">DESCRIPTION</span></span>
<span data-ttu-id="026d3-110">刪除 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="026d3-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="026d3-111">示例</span><span class="sxs-lookup"><span data-stu-id="026d3-111">EXAMPLES</span></span>

### <span data-ttu-id="026d3-112">範例1：依物件識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="026d3-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="026d3-113">從租使用者移除物件 id 為 ' b4cd1619-80b3-4cfb-9f8f-9f2333425738」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="026d3-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="026d3-114">範例2：依應用程式識別碼移除應用程式</span><span class="sxs-lookup"><span data-stu-id="026d3-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="026d3-115">從租使用者移除含應用程式識別碼 ' f9c5ea4f-28f0-401a-a491-491a037fa346」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="026d3-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="026d3-116">範例3：透過管道移除應用程式</span><span class="sxs-lookup"><span data-stu-id="026d3-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="026d3-117">取得 b4cd1619-80b3-4cfb-9f8f-9f2333425738 Cmdlet 的物件識別碼 '」和 Remove-AzADApplication 管道，以從租使用者中移除應用程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="026d3-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="026d3-118">參數</span><span class="sxs-lookup"><span data-stu-id="026d3-118">PARAMETERS</span></span>

### <span data-ttu-id="026d3-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="026d3-119">-ApplicationId</span></span>
<span data-ttu-id="026d3-120">要移除之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="026d3-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="026d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026d3-121">-DefaultProfile</span></span>
<span data-ttu-id="026d3-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="026d3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="026d3-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="026d3-123">-DisplayName</span></span>
<span data-ttu-id="026d3-124">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="026d3-124">The display name of the application.</span></span>

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

### <span data-ttu-id="026d3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="026d3-125">-Force</span></span>
<span data-ttu-id="026d3-126">切換以刪除應用程式而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="026d3-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="026d3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="026d3-127">-InputObject</span></span>
<span data-ttu-id="026d3-128">代表要移除之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="026d3-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="026d3-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="026d3-129">-ObjectId</span></span>
<span data-ttu-id="026d3-130">要刪除之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="026d3-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="026d3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="026d3-131">-PassThru</span></span>
<span data-ttu-id="026d3-132">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="026d3-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="026d3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="026d3-133">-Confirm</span></span>
<span data-ttu-id="026d3-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="026d3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="026d3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="026d3-135">-WhatIf</span></span>
<span data-ttu-id="026d3-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="026d3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="026d3-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="026d3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="026d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026d3-138">CommonParameters</span></span>
<span data-ttu-id="026d3-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="026d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026d3-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="026d3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026d3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="026d3-141">INPUTS</span></span>

### <span data-ttu-id="026d3-142">System.object</span><span class="sxs-lookup"><span data-stu-id="026d3-142">System.String</span></span>

### <span data-ttu-id="026d3-143">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="026d3-143">System.Guid</span></span>

### <span data-ttu-id="026d3-144">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="026d3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="026d3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="026d3-145">OUTPUTS</span></span>

### <span data-ttu-id="026d3-146">System.object</span><span class="sxs-lookup"><span data-stu-id="026d3-146">System.Boolean</span></span>

## <span data-ttu-id="026d3-147">筆記</span><span class="sxs-lookup"><span data-stu-id="026d3-147">NOTES</span></span>
<span data-ttu-id="026d3-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="026d3-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="026d3-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="026d3-149">RELATED LINKS</span></span>

[<span data-ttu-id="026d3-150">新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="026d3-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="026d3-151">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="026d3-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="026d3-152">更新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="026d3-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="026d3-153">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="026d3-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

