---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450936"
---
# <span data-ttu-id="5ce4d-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="5ce4d-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="5ce4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce4d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce4d-103">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce4d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ce4d-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce4d-106">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="5ce4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ce4d-107">EXAMPLES</span></span>

### <span data-ttu-id="5ce4d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5ce4d-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="5ce4d-109">Cmdlet 會更新 Facebook 身分識別提供者的用戶端密碼;</span><span class="sxs-lookup"><span data-stu-id="5ce4d-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="5ce4d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ce4d-110">PARAMETERS</span></span>

### <span data-ttu-id="5ce4d-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="5ce4d-111">-AllowedTenants</span></span>
<span data-ttu-id="5ce4d-112">允許的 Azure Active Directory 租使用者清單。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="5ce4d-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5ce4d-113">-ClientId</span></span>
<span data-ttu-id="5ce4d-114">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="5ce4d-115">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4d-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5ce4d-116">-ClientSecret</span></span>
<span data-ttu-id="5ce4d-117">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="5ce4d-118">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4d-119">-內容</span><span class="sxs-lookup"><span data-stu-id="5ce4d-119">-Context</span></span>
<span data-ttu-id="5ce4d-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5ce4d-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="5ce4d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ce4d-122">-PassThru</span></span>
<span data-ttu-id="5ce4d-123">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementIdentityProvider** 。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4d-124">-類型</span><span class="sxs-lookup"><span data-stu-id="5ce4d-124">-Type</span></span>
<span data-ttu-id="5ce4d-125">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="5ce4d-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-126">This parameter is required.</span></span>

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

### <span data-ttu-id="5ce4d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5ce4d-127">-Confirm</span></span>
<span data-ttu-id="5ce4d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce4d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce4d-129">-WhatIf</span></span>
<span data-ttu-id="5ce4d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ce4d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce4d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce4d-132">-DefaultProfile</span></span>
<span data-ttu-id="5ce4d-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ce4d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce4d-134">CommonParameters</span></span>
<span data-ttu-id="5ce4d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce4d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ce4d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce4d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce4d-137">INPUTS</span></span>

## <span data-ttu-id="5ce4d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce4d-138">OUTPUTS</span></span>

### <span data-ttu-id="5ce4d-139">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5ce4d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="5ce4d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce4d-140">NOTES</span></span>

## <span data-ttu-id="5ce4d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce4d-141">RELATED LINKS</span></span>

[<span data-ttu-id="5ce4d-142">新-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="5ce4d-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="5ce4d-143">AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="5ce4d-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="5ce4d-144">移除-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="5ce4d-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
