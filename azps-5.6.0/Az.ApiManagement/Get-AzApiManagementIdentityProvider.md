---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f09dc3079335521f099af5cbd397b6a56a57a7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903901"
---
# <span data-ttu-id="54426-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="54426-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="54426-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54426-102">SYNOPSIS</span></span>
<span data-ttu-id="54426-103">取得身分識別提供者組組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="54426-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="54426-104">語法</span><span class="sxs-lookup"><span data-stu-id="54426-104">SYNTAX</span></span>

### <span data-ttu-id="54426-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="54426-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54426-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="54426-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54426-107">描述</span><span class="sxs-lookup"><span data-stu-id="54426-107">DESCRIPTION</span></span>
<span data-ttu-id="54426-108">取得身分識別提供者組組詳細資料。</span><span class="sxs-lookup"><span data-stu-id="54426-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="54426-109">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="54426-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="54426-110">若要取得用戶端密碼，請使用 **Get-AzApiManagementIdentityProviderClientSecret。**</span><span class="sxs-lookup"><span data-stu-id="54426-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="54426-111">例子</span><span class="sxs-lookup"><span data-stu-id="54426-111">EXAMPLES</span></span>

### <span data-ttu-id="54426-112">範例 1：取得所有身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="54426-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="54426-113">取得服務上的所有身分識別提供者組配置。</span><span class="sxs-lookup"><span data-stu-id="54426-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="54426-114">範例 2：取得 AAD 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="54426-114">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="54426-115">獲得 Azure Active Directory 的身分識別提供者組配置。</span><span class="sxs-lookup"><span data-stu-id="54426-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="54426-116">範例 3：取得 AAD B2C 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="54426-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="54426-117">獲得 Azure Active Directory 的身分識別提供者組配置。</span><span class="sxs-lookup"><span data-stu-id="54426-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="54426-118">參數</span><span class="sxs-lookup"><span data-stu-id="54426-118">PARAMETERS</span></span>

### <span data-ttu-id="54426-119">-內容</span><span class="sxs-lookup"><span data-stu-id="54426-119">-Context</span></span>
<span data-ttu-id="54426-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="54426-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="54426-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="54426-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54426-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54426-122">-DefaultProfile</span></span>
<span data-ttu-id="54426-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54426-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54426-124">-類型</span><span class="sxs-lookup"><span data-stu-id="54426-124">-Type</span></span>
<span data-ttu-id="54426-125">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54426-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="54426-126">如果指定，會嘗試根據識別碼尋找身分識別提供者組。</span><span class="sxs-lookup"><span data-stu-id="54426-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="54426-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="54426-127">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54426-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54426-128">CommonParameters</span></span>
<span data-ttu-id="54426-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54426-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54426-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54426-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54426-131">輸入</span><span class="sxs-lookup"><span data-stu-id="54426-131">INPUTS</span></span>

### <span data-ttu-id="54426-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="54426-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="54426-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="54426-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="54426-134">輸出</span><span class="sxs-lookup"><span data-stu-id="54426-134">OUTPUTS</span></span>

### <span data-ttu-id="54426-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="54426-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="54426-136">筆記</span><span class="sxs-lookup"><span data-stu-id="54426-136">NOTES</span></span>

## <span data-ttu-id="54426-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="54426-137">RELATED LINKS</span></span>
