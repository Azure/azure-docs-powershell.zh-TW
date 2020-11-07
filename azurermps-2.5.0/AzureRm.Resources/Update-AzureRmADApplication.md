---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: bf9f993724de9ed20587a3f4ca136c3531689401
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800673"
---
# <span data-ttu-id="1ca90-101">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1ca90-101">Update-AzureRmADApplication</span></span>

## <span data-ttu-id="1ca90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ca90-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca90-103">更新現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1ca90-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ca90-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ca90-104">SYNTAX</span></span>

### <span data-ttu-id="1ca90-105">ApplicationObjectIdWithUpdateParamsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1ca90-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzureRmADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca90-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ca90-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca90-108">說明</span><span class="sxs-lookup"><span data-stu-id="1ca90-108">DESCRIPTION</span></span>
<span data-ttu-id="1ca90-109">更新現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1ca90-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="1ca90-110">若要更新與此應用程式相關聯的認證，請使用 New-AzureRmADAppCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ca90-110">To update the credentials associated with this application, please use the New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="1ca90-111">示例</span><span class="sxs-lookup"><span data-stu-id="1ca90-111">EXAMPLES</span></span>

### <span data-ttu-id="1ca90-112">範例 1-更新應用程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1ca90-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="1ca90-113">將物件 id ' fb7b3405-ca44-4b5b-8584-12392f5d96d7」的應用程式顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="1ca90-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="1ca90-114">範例 2-更新應用程式的所有屬性</span><span class="sxs-lookup"><span data-stu-id="1ca90-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="1ca90-115">使用物件 id ' fb7b3405-ca44-4b5b-8584-12392f5d96d7」更新應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ca90-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="1ca90-116">範例 3-使用管道更新應用程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1ca90-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzureRmADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="1ca90-117">取得 fb7b3405-ca44-4b5b-8584-12392f5d96d7 Cmdlet 之物件 id 為「」和 Update-AzureRmADApplication 管道的應用程式，以將應用程式的顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="1ca90-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzureRmADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="1ca90-118">參數</span><span class="sxs-lookup"><span data-stu-id="1ca90-118">PARAMETERS</span></span>

### <span data-ttu-id="1ca90-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1ca90-119">-ApplicationId</span></span>
<span data-ttu-id="1ca90-120">要更新之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ca90-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="1ca90-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="1ca90-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="1ca90-122">如果應用程式與其他承租人共用，則為 True，否則為 false。否則為 false。</span><span class="sxs-lookup"><span data-stu-id="1ca90-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="1ca90-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca90-123">-DefaultProfile</span></span>
<span data-ttu-id="1ca90-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ca90-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ca90-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ca90-125">-DisplayName</span></span>
<span data-ttu-id="1ca90-126">要更新之應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca90-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="1ca90-127">-首頁</span><span class="sxs-lookup"><span data-stu-id="1ca90-127">-HomePage</span></span>
<span data-ttu-id="1ca90-128">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="1ca90-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="1ca90-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1ca90-129">-IdentifierUri</span></span>
<span data-ttu-id="1ca90-130">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="1ca90-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="1ca90-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ca90-131">-InputObject</span></span>
<span data-ttu-id="1ca90-132">代表要更新之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="1ca90-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1ca90-133">-ObjectId</span></span>
<span data-ttu-id="1ca90-134">要更新之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ca90-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca90-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="1ca90-135">-ReplyUrl</span></span>
<span data-ttu-id="1ca90-136">指定傳送給使用者權杖以進行登入的 Url，或將 OAuth 2.0 授權碼及存取權杖傳送至的重新導向 Uri。</span><span class="sxs-lookup"><span data-stu-id="1ca90-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="1ca90-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1ca90-137">-Confirm</span></span>
<span data-ttu-id="1ca90-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ca90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca90-139">-WhatIf</span></span>
<span data-ttu-id="1ca90-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ca90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca90-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ca90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca90-142">CommonParameters</span></span>
<span data-ttu-id="1ca90-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ca90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca90-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ca90-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca90-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1ca90-145">INPUTS</span></span>

### <span data-ttu-id="1ca90-146">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="1ca90-146">System.Guid</span></span>

### <span data-ttu-id="1ca90-147">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1ca90-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1ca90-148">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1ca90-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1ca90-149">System.object</span><span class="sxs-lookup"><span data-stu-id="1ca90-149">System.String</span></span>

### <span data-ttu-id="1ca90-150">System.object []</span><span class="sxs-lookup"><span data-stu-id="1ca90-150">System.String[]</span></span>

### <span data-ttu-id="1ca90-151">System.object</span><span class="sxs-lookup"><span data-stu-id="1ca90-151">System.Boolean</span></span>

## <span data-ttu-id="1ca90-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1ca90-152">OUTPUTS</span></span>

### <span data-ttu-id="1ca90-153">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1ca90-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="1ca90-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1ca90-154">NOTES</span></span>

## <span data-ttu-id="1ca90-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ca90-155">RELATED LINKS</span></span>
