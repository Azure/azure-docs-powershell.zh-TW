---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957875"
---
# <span data-ttu-id="f6a11-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f6a11-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f6a11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6a11-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a11-103">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6a11-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f6a11-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6a11-104">SYNTAX</span></span>

### <span data-ttu-id="f6a11-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="f6a11-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a11-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="f6a11-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a11-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6a11-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a11-108">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6a11-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f6a11-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6a11-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a11-110">範例1：取得所有身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="f6a11-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="f6a11-111">取得服務上的所有身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="f6a11-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="f6a11-112">範例2：取得 AAD 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="f6a11-112">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="f6a11-113">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="f6a11-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="f6a11-114">範例3：取得 AAD B2C 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="f6a11-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="f6a11-115">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="f6a11-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="f6a11-116">參數</span><span class="sxs-lookup"><span data-stu-id="f6a11-116">PARAMETERS</span></span>

### <span data-ttu-id="f6a11-117">-內容</span><span class="sxs-lookup"><span data-stu-id="f6a11-117">-Context</span></span>
<span data-ttu-id="f6a11-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f6a11-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f6a11-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f6a11-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f6a11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a11-120">-DefaultProfile</span></span>
<span data-ttu-id="f6a11-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6a11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a11-122">-類型</span><span class="sxs-lookup"><span data-stu-id="f6a11-122">-Type</span></span>
<span data-ttu-id="f6a11-123">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a11-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f6a11-124">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="f6a11-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f6a11-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f6a11-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="f6a11-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a11-126">CommonParameters</span></span>
<span data-ttu-id="f6a11-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6a11-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a11-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6a11-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a11-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f6a11-129">INPUTS</span></span>

### <span data-ttu-id="f6a11-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6a11-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f6a11-131">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6a11-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="f6a11-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f6a11-132">OUTPUTS</span></span>

### <span data-ttu-id="f6a11-133">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6a11-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f6a11-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f6a11-134">NOTES</span></span>

## <span data-ttu-id="f6a11-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6a11-135">RELATED LINKS</span></span>
