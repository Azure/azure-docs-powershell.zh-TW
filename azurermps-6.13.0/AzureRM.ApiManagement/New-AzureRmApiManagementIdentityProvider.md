---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d0883edb698000ae0aaff957899a03e9936e4d93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450348"
---
# <span data-ttu-id="40c8e-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="40c8e-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="40c8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="40c8e-103">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="40c8e-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="40c8e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40c8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="40c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="40c8e-106">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="40c8e-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="40c8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="40c8e-107">EXAMPLES</span></span>

### <span data-ttu-id="40c8e-108">範例1：將 Facebook 配置為開發人員入口網站登錄的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="40c8e-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="40c8e-109">這個命令會在 ApiManagement 服務的開發人員入口網站上，將 Facebook 身分識別為已接受的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="40c8e-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="40c8e-110">這會採用 Facebook 應用程式的 ClientId 與 ClientSecret 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="40c8e-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="40c8e-111">參數</span><span class="sxs-lookup"><span data-stu-id="40c8e-111">PARAMETERS</span></span>

### <span data-ttu-id="40c8e-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="40c8e-112">-AllowedTenants</span></span>
<span data-ttu-id="40c8e-113">允許的 Azure Active Directory 承租人清單</span><span class="sxs-lookup"><span data-stu-id="40c8e-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c8e-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="40c8e-114">-ClientId</span></span>
<span data-ttu-id="40c8e-115">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="40c8e-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="40c8e-116">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="40c8e-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c8e-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="40c8e-117">-ClientSecret</span></span>
<span data-ttu-id="40c8e-118">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="40c8e-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="40c8e-119">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="40c8e-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c8e-120">-內容</span><span class="sxs-lookup"><span data-stu-id="40c8e-120">-Context</span></span>
<span data-ttu-id="40c8e-121">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="40c8e-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="40c8e-122">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="40c8e-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c8e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c8e-123">-DefaultProfile</span></span>
<span data-ttu-id="40c8e-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40c8e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40c8e-125">-類型</span><span class="sxs-lookup"><span data-stu-id="40c8e-125">-Type</span></span>
<span data-ttu-id="40c8e-126">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40c8e-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="40c8e-127">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="40c8e-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="40c8e-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40c8e-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c8e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="40c8e-129">-Confirm</span></span>
<span data-ttu-id="40c8e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40c8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c8e-131">-WhatIf</span></span>
<span data-ttu-id="40c8e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40c8e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40c8e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40c8e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c8e-134">CommonParameters</span></span>
<span data-ttu-id="40c8e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40c8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c8e-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40c8e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c8e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="40c8e-137">INPUTS</span></span>

### <span data-ttu-id="40c8e-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40c8e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40c8e-139">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40c8e-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="40c8e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="40c8e-140">System.String</span></span>

### <span data-ttu-id="40c8e-141">System.object []</span><span class="sxs-lookup"><span data-stu-id="40c8e-141">System.String[]</span></span>

## <span data-ttu-id="40c8e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="40c8e-142">OUTPUTS</span></span>

### <span data-ttu-id="40c8e-143">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40c8e-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="40c8e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="40c8e-144">NOTES</span></span>

## <span data-ttu-id="40c8e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="40c8e-145">RELATED LINKS</span></span>

[<span data-ttu-id="40c8e-146">AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="40c8e-146">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="40c8e-147">移除-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="40c8e-147">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="40c8e-148">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="40c8e-148">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
