---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 93e2b62cf1261b20df1ea6c90d48caa1e1d88ec2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909470"
---
# <span data-ttu-id="3a7f5-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3a7f5-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="3a7f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7f5-103">從應用程式移除認證。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="3a7f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a7f5-104">SYNTAX</span></span>

### <span data-ttu-id="3a7f5-105">ApplicationObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a7f5-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7f5-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7f5-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7f5-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7f5-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a7f5-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7f5-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7f5-109">描述</span><span class="sxs-lookup"><span data-stu-id="3a7f5-109">DESCRIPTION</span></span>
<span data-ttu-id="3a7f5-110">在Remove-AzADAppCredential或認證金鑰切換到期時，可以使用 Remove-AzADAppCredential Cmdlet 從應用程式移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="3a7f5-111">提供物件識別碼或 AppId 以識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="3a7f5-112">要移除的認證會以金鑰識別碼識別。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="3a7f5-113">例子</span><span class="sxs-lookup"><span data-stu-id="3a7f5-113">EXAMPLES</span></span>

### <span data-ttu-id="3a7f5-114">範例 1：從應用程式移除特定認證</span><span class="sxs-lookup"><span data-stu-id="3a7f5-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="3a7f5-115">使用物件識別碼為 '7663d3fb-6f86-4352-9e66d-cf9d50d5ee82'的應用程式移除具有金鑰識別碼 '9044423a-60a3-45ac-9ab1-09534157ebb'的認證。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="3a7f5-116">範例 2：移除應用程式的所有認證</span><span class="sxs-lookup"><span data-stu-id="3a7f5-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="3a7f5-117">移除應用程式的所有認證，其應用程式識別碼為 '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="3a7f5-118">範例 3：使用管道移除所有認證</span><span class="sxs-lookup"><span data-stu-id="3a7f5-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="3a7f5-119">使用物件識別碼 '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' 和管道到 Remove-AzADAppCredential Cmdlet 的應用程式，並移除該應用程式的所有認證。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="3a7f5-120">參數</span><span class="sxs-lookup"><span data-stu-id="3a7f5-120">PARAMETERS</span></span>

### <span data-ttu-id="3a7f5-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3a7f5-121">-ApplicationId</span></span>
<span data-ttu-id="3a7f5-122">要從移除認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f5-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="3a7f5-123">-ApplicationObject</span></span>
<span data-ttu-id="3a7f5-124">要從移除認證的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7f5-125">-DefaultProfile</span></span>
<span data-ttu-id="3a7f5-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3a7f5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a7f5-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a7f5-127">-DisplayName</span></span>
<span data-ttu-id="3a7f5-128">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-128">The display name of the application.</span></span>

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

### <span data-ttu-id="3a7f5-129">-強制</span><span class="sxs-lookup"><span data-stu-id="3a7f5-129">-Force</span></span>
<span data-ttu-id="3a7f5-130">切換以刪除認證而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="3a7f5-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3a7f5-131">-KeyId</span></span>
<span data-ttu-id="3a7f5-132">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="3a7f5-133">您可以使用 Cmdlet 取得應用程式Get-AzADAppCredential識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f5-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3a7f5-134">-ObjectId</span></span>
<span data-ttu-id="3a7f5-135">要從移除認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a7f5-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a7f5-136">-PassThru</span></span>
<span data-ttu-id="3a7f5-137">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3a7f5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="3a7f5-138">-Confirm</span></span>
<span data-ttu-id="3a7f5-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7f5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7f5-140">-WhatIf</span></span>
<span data-ttu-id="3a7f5-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a7f5-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7f5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7f5-143">CommonParameters</span></span>
<span data-ttu-id="3a7f5-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a7f5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7f5-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a7f5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7f5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="3a7f5-146">INPUTS</span></span>

### <span data-ttu-id="3a7f5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3a7f5-147">System.String</span></span>

### <span data-ttu-id="3a7f5-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3a7f5-148">System.Guid</span></span>

### <span data-ttu-id="3a7f5-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3a7f5-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3a7f5-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3a7f5-150">OUTPUTS</span></span>

### <span data-ttu-id="3a7f5-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a7f5-151">System.Boolean</span></span>

## <span data-ttu-id="3a7f5-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3a7f5-152">NOTES</span></span>

## <span data-ttu-id="3a7f5-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a7f5-153">RELATED LINKS</span></span>

[<span data-ttu-id="3a7f5-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3a7f5-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="3a7f5-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3a7f5-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="3a7f5-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3a7f5-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
