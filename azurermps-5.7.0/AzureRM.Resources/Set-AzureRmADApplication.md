---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454120"
---
# <span data-ttu-id="d41c6-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d41c6-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="d41c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d41c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d41c6-103">更新現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d41c6-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d41c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d41c6-104">SYNTAX</span></span>

### <span data-ttu-id="d41c6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41c6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41c6-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41c6-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d41c6-107">說明</span><span class="sxs-lookup"><span data-stu-id="d41c6-107">DESCRIPTION</span></span>
<span data-ttu-id="d41c6-108">更新現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d41c6-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="d41c6-109">若要更新與此應用程式相關聯的認證，請使用 New-AzureRmADAppCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d41c6-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="d41c6-110">示例</span><span class="sxs-lookup"><span data-stu-id="d41c6-110">EXAMPLES</span></span>

### <span data-ttu-id="d41c6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d41c6-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="d41c6-112">使用 objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7" 更新現有 azure active directory 應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="d41c6-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="d41c6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d41c6-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="d41c6-114">使用 objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7" 更新現有 azure active directory 應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d41c6-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="d41c6-115">參數</span><span class="sxs-lookup"><span data-stu-id="d41c6-115">PARAMETERS</span></span>

### <span data-ttu-id="d41c6-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d41c6-116">-ApplicationId</span></span>
<span data-ttu-id="d41c6-117">要更新的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="d41c6-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="d41c6-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="d41c6-119">指定應用程式是否更新為單一租使用者或多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="d41c6-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41c6-120">-DefaultProfile</span></span>
<span data-ttu-id="d41c6-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d41c6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d41c6-122">-DisplayName</span></span>
<span data-ttu-id="d41c6-123">應用程式的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d41c6-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-124">-首頁</span><span class="sxs-lookup"><span data-stu-id="d41c6-124">-HomePage</span></span>
<span data-ttu-id="d41c6-125">應用程式首頁的新 URL。</span><span class="sxs-lookup"><span data-stu-id="d41c6-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="d41c6-126">-IdentifierUris</span></span>
<span data-ttu-id="d41c6-127">識別應用程式的新 Uri。</span><span class="sxs-lookup"><span data-stu-id="d41c6-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d41c6-128">-ObjectId</span></span>
<span data-ttu-id="d41c6-129">要更新之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d41c6-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="d41c6-130">-ReplyUrls</span></span>
<span data-ttu-id="d41c6-131">應用程式的新回復 url。</span><span class="sxs-lookup"><span data-stu-id="d41c6-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d41c6-132">-Confirm</span></span>
<span data-ttu-id="d41c6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d41c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d41c6-134">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d41c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41c6-135">CommonParameters</span></span>
<span data-ttu-id="d41c6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d41c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41c6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d41c6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41c6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d41c6-138">INPUTS</span></span>

### <span data-ttu-id="d41c6-139">所有</span><span class="sxs-lookup"><span data-stu-id="d41c6-139">None</span></span>
<span data-ttu-id="d41c6-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d41c6-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d41c6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d41c6-141">OUTPUTS</span></span>

### <span data-ttu-id="d41c6-142">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d41c6-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d41c6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d41c6-143">NOTES</span></span>

## <span data-ttu-id="d41c6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d41c6-144">RELATED LINKS</span></span>

[<span data-ttu-id="d41c6-145">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d41c6-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="d41c6-146">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d41c6-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="d41c6-147">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d41c6-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="d41c6-148">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d41c6-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="d41c6-149">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d41c6-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="d41c6-150">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d41c6-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

