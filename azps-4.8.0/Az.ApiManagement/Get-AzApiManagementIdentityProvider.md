---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971342"
---
# <span data-ttu-id="306c3-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="306c3-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="306c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="306c3-102">SYNOPSIS</span></span>
<span data-ttu-id="306c3-103">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="306c3-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="306c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="306c3-104">SYNTAX</span></span>

### <span data-ttu-id="306c3-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="306c3-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="306c3-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="306c3-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="306c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="306c3-107">DESCRIPTION</span></span>
<span data-ttu-id="306c3-108">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="306c3-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="306c3-109">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="306c3-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="306c3-110">若要取得用戶端密碼，請使用 **AzApiManagementIdentityProviderClientSecret** 。</span><span class="sxs-lookup"><span data-stu-id="306c3-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="306c3-111">示例</span><span class="sxs-lookup"><span data-stu-id="306c3-111">EXAMPLES</span></span>

### <span data-ttu-id="306c3-112">範例1：取得所有身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="306c3-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="306c3-113">取得服務上的所有身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="306c3-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="306c3-114">範例2：取得 AAD 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="306c3-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="306c3-115">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="306c3-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="306c3-116">範例3：取得 AAD B2C 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="306c3-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="306c3-117">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="306c3-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="306c3-118">參數</span><span class="sxs-lookup"><span data-stu-id="306c3-118">PARAMETERS</span></span>

### <span data-ttu-id="306c3-119">-內容</span><span class="sxs-lookup"><span data-stu-id="306c3-119">-Context</span></span>
<span data-ttu-id="306c3-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="306c3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="306c3-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="306c3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="306c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306c3-122">-DefaultProfile</span></span>
<span data-ttu-id="306c3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="306c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="306c3-124">-類型</span><span class="sxs-lookup"><span data-stu-id="306c3-124">-Type</span></span>
<span data-ttu-id="306c3-125">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="306c3-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="306c3-126">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="306c3-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="306c3-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="306c3-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="306c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306c3-128">CommonParameters</span></span>
<span data-ttu-id="306c3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="306c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306c3-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="306c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306c3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="306c3-131">INPUTS</span></span>

### <span data-ttu-id="306c3-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="306c3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="306c3-133">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="306c3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="306c3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="306c3-134">OUTPUTS</span></span>

### <span data-ttu-id="306c3-135">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="306c3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="306c3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="306c3-136">NOTES</span></span>

## <span data-ttu-id="306c3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="306c3-137">RELATED LINKS</span></span>
