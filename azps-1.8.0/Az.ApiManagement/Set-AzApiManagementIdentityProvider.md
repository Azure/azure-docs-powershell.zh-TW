---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788761"
---
# <span data-ttu-id="58a10-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="58a10-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="58a10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58a10-102">SYNOPSIS</span></span>
<span data-ttu-id="58a10-103">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="58a10-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="58a10-104">句法</span><span class="sxs-lookup"><span data-stu-id="58a10-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58a10-105">說明</span><span class="sxs-lookup"><span data-stu-id="58a10-105">DESCRIPTION</span></span>
<span data-ttu-id="58a10-106">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="58a10-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="58a10-107">示例</span><span class="sxs-lookup"><span data-stu-id="58a10-107">EXAMPLES</span></span>

### <span data-ttu-id="58a10-108">範例1</span><span class="sxs-lookup"><span data-stu-id="58a10-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="58a10-109">Cmdlet 會更新 Facebook 身分識別提供者的用戶端密碼;</span><span class="sxs-lookup"><span data-stu-id="58a10-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="58a10-110">參數</span><span class="sxs-lookup"><span data-stu-id="58a10-110">PARAMETERS</span></span>

### <span data-ttu-id="58a10-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="58a10-111">-AllowedTenants</span></span>
<span data-ttu-id="58a10-112">允許的 Azure Active Directory 租使用者清單。</span><span class="sxs-lookup"><span data-stu-id="58a10-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="58a10-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="58a10-113">-ClientId</span></span>
<span data-ttu-id="58a10-114">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="58a10-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="58a10-115">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="58a10-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="58a10-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="58a10-116">-ClientSecret</span></span>
<span data-ttu-id="58a10-117">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="58a10-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="58a10-118">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="58a10-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="58a10-119">-內容</span><span class="sxs-lookup"><span data-stu-id="58a10-119">-Context</span></span>
<span data-ttu-id="58a10-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="58a10-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="58a10-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="58a10-121">This parameter is required.</span></span>

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

### <span data-ttu-id="58a10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a10-122">-DefaultProfile</span></span>
<span data-ttu-id="58a10-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58a10-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58a10-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58a10-124">-PassThru</span></span>
<span data-ttu-id="58a10-125">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementIdentityProvider** 。</span><span class="sxs-lookup"><span data-stu-id="58a10-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="58a10-126">-類型</span><span class="sxs-lookup"><span data-stu-id="58a10-126">-Type</span></span>
<span data-ttu-id="58a10-127">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="58a10-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="58a10-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="58a10-128">This parameter is required.</span></span>

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

### <span data-ttu-id="58a10-129">-確認</span><span class="sxs-lookup"><span data-stu-id="58a10-129">-Confirm</span></span>
<span data-ttu-id="58a10-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58a10-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a10-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a10-131">-WhatIf</span></span>
<span data-ttu-id="58a10-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58a10-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58a10-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58a10-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a10-134">CommonParameters</span></span>
<span data-ttu-id="58a10-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58a10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a10-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58a10-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a10-137">輸入</span><span class="sxs-lookup"><span data-stu-id="58a10-137">INPUTS</span></span>

### <span data-ttu-id="58a10-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="58a10-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="58a10-139">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="58a10-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="58a10-140">System.object</span><span class="sxs-lookup"><span data-stu-id="58a10-140">System.String</span></span>

### <span data-ttu-id="58a10-141">System.object []</span><span class="sxs-lookup"><span data-stu-id="58a10-141">System.String[]</span></span>

### <span data-ttu-id="58a10-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="58a10-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58a10-143">輸出</span><span class="sxs-lookup"><span data-stu-id="58a10-143">OUTPUTS</span></span>

### <span data-ttu-id="58a10-144">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="58a10-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="58a10-145">筆記</span><span class="sxs-lookup"><span data-stu-id="58a10-145">NOTES</span></span>

## <span data-ttu-id="58a10-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="58a10-146">RELATED LINKS</span></span>

[<span data-ttu-id="58a10-147">新-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="58a10-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="58a10-148">AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="58a10-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="58a10-149">移除-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="58a10-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
