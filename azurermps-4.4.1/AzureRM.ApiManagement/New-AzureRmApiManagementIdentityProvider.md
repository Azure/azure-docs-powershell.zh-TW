---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d6536c63ab3241e999c87dfb025205571c29596c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450103"
---
# <span data-ttu-id="3629b-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3629b-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="3629b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3629b-102">SYNOPSIS</span></span>
<span data-ttu-id="3629b-103">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="3629b-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3629b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3629b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3629b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3629b-105">DESCRIPTION</span></span>
<span data-ttu-id="3629b-106">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="3629b-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="3629b-107">示例</span><span class="sxs-lookup"><span data-stu-id="3629b-107">EXAMPLES</span></span>

### <span data-ttu-id="3629b-108">範例1：將 Facebook 配置為開發人員入口網站登錄的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="3629b-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="3629b-109">這個命令會在 ApiManagement 服務的開發人員入口網站上，將 Facebook 身分識別為已接受的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="3629b-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="3629b-110">這會採用 Facebook 應用程式的 ClientId 與 ClientSecret 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="3629b-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="3629b-111">參數</span><span class="sxs-lookup"><span data-stu-id="3629b-111">PARAMETERS</span></span>

### <span data-ttu-id="3629b-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="3629b-112">-AllowedTenants</span></span>
<span data-ttu-id="3629b-113">允許的 Azure Active Directory 承租人清單</span><span class="sxs-lookup"><span data-stu-id="3629b-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="3629b-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="3629b-114">-ClientId</span></span>
<span data-ttu-id="3629b-115">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="3629b-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="3629b-116">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="3629b-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="3629b-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3629b-117">-ClientSecret</span></span>
<span data-ttu-id="3629b-118">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="3629b-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="3629b-119">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="3629b-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="3629b-120">-內容</span><span class="sxs-lookup"><span data-stu-id="3629b-120">-Context</span></span>
<span data-ttu-id="3629b-121">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="3629b-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3629b-122">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3629b-122">This parameter is required.</span></span>

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

### <span data-ttu-id="3629b-123">-類型</span><span class="sxs-lookup"><span data-stu-id="3629b-123">-Type</span></span>
<span data-ttu-id="3629b-124">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3629b-124">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="3629b-125">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="3629b-125">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="3629b-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3629b-126">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3629b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3629b-127">-Confirm</span></span>
<span data-ttu-id="3629b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3629b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3629b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3629b-129">-WhatIf</span></span>
<span data-ttu-id="3629b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3629b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3629b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3629b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3629b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3629b-132">-DefaultProfile</span></span>
<span data-ttu-id="3629b-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3629b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3629b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3629b-134">CommonParameters</span></span>
<span data-ttu-id="3629b-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3629b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3629b-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3629b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3629b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3629b-137">INPUTS</span></span>

## <span data-ttu-id="3629b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3629b-138">OUTPUTS</span></span>

### <span data-ttu-id="3629b-139">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3629b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="3629b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3629b-140">NOTES</span></span>

## <span data-ttu-id="3629b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3629b-141">RELATED LINKS</span></span>

[<span data-ttu-id="3629b-142">AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3629b-142">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="3629b-143">移除-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3629b-143">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="3629b-144">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3629b-144">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
