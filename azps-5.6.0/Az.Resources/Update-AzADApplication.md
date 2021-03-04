---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 329620701c4afb52bdebd145ef461c7d311c26a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913665"
---
# <span data-ttu-id="57828-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="57828-101">Update-AzADApplication</span></span>

## <span data-ttu-id="57828-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57828-102">SYNOPSIS</span></span>
<span data-ttu-id="57828-103">更新現有的 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="57828-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="57828-104">語法</span><span class="sxs-lookup"><span data-stu-id="57828-104">SYNTAX</span></span>

### <span data-ttu-id="57828-105">ApplicationObjectIdWithUpdateParamsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57828-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57828-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="57828-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57828-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="57828-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57828-108">描述</span><span class="sxs-lookup"><span data-stu-id="57828-108">DESCRIPTION</span></span>
<span data-ttu-id="57828-109">更新現有的 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="57828-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="57828-110">若要更新與此應用程式相關聯的認證，請使用 New-AzADAppCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57828-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="57828-111">例子</span><span class="sxs-lookup"><span data-stu-id="57828-111">EXAMPLES</span></span>

### <span data-ttu-id="57828-112">範例 1 - 更新應用程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="57828-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="57828-113">將應用程式顯示名稱與物件識別碼 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' 更新為 'MyNewDisplayName'。</span><span class="sxs-lookup"><span data-stu-id="57828-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="57828-114">範例 2 - 更新應用程式的所有屬性</span><span class="sxs-lookup"><span data-stu-id="57828-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="57828-115">以物件識別碼 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'更新應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="57828-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="57828-116">範例 3 - 使用管道更新應用程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="57828-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="57828-117">使用物件識別碼 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' 和管道到 Update-AzADApplication Cmdlet 的應用程式，將應用程式的顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="57828-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="57828-118">參數</span><span class="sxs-lookup"><span data-stu-id="57828-118">PARAMETERS</span></span>

### <span data-ttu-id="57828-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="57828-119">-ApplicationId</span></span>
<span data-ttu-id="57828-120">要更新之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="57828-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-121">-AvailableToTentenants</span><span class="sxs-lookup"><span data-stu-id="57828-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="57828-122">如果應用程式與其他租使用者共用，則為 True;否則，為 False。</span><span class="sxs-lookup"><span data-stu-id="57828-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57828-123">-DefaultProfile</span></span>
<span data-ttu-id="57828-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57828-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57828-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57828-125">-DisplayName</span></span>
<span data-ttu-id="57828-126">要更新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="57828-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="57828-127">-HomePage</span></span>
<span data-ttu-id="57828-128">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="57828-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="57828-129">-IdentifierUri</span></span>
<span data-ttu-id="57828-130">識別應用程式的 URI。</span><span class="sxs-lookup"><span data-stu-id="57828-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57828-131">-InputObject</span></span>
<span data-ttu-id="57828-132">代表要更新之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="57828-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="57828-133">-ObjectId</span></span>
<span data-ttu-id="57828-134">要更新之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="57828-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="57828-135">-ReplyUrl</span></span>
<span data-ttu-id="57828-136">指定使用者權杖要送出以用於登錄的 URL，或 OAuth 2.0 授權碼和存取權杖所寄往的重新導向 URI。</span><span class="sxs-lookup"><span data-stu-id="57828-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57828-137">-確認</span><span class="sxs-lookup"><span data-stu-id="57828-137">-Confirm</span></span>
<span data-ttu-id="57828-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57828-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57828-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57828-139">-WhatIf</span></span>
<span data-ttu-id="57828-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57828-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57828-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57828-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57828-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57828-142">CommonParameters</span></span>
<span data-ttu-id="57828-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57828-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57828-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57828-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57828-145">輸入</span><span class="sxs-lookup"><span data-stu-id="57828-145">INPUTS</span></span>

### <span data-ttu-id="57828-146">System.String</span><span class="sxs-lookup"><span data-stu-id="57828-146">System.String</span></span>

### <span data-ttu-id="57828-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="57828-147">System.Guid</span></span>

### <span data-ttu-id="57828-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="57828-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="57828-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="57828-149">System.String[]</span></span>

### <span data-ttu-id="57828-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57828-150">System.Boolean</span></span>

## <span data-ttu-id="57828-151">輸出</span><span class="sxs-lookup"><span data-stu-id="57828-151">OUTPUTS</span></span>

### <span data-ttu-id="57828-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="57828-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="57828-153">筆記</span><span class="sxs-lookup"><span data-stu-id="57828-153">NOTES</span></span>

## <span data-ttu-id="57828-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="57828-154">RELATED LINKS</span></span>
