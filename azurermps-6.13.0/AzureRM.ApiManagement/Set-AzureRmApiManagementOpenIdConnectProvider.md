---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445816"
---
# <span data-ttu-id="3770b-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3770b-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3770b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3770b-102">SYNOPSIS</span></span>
<span data-ttu-id="3770b-103">修改 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="3770b-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3770b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3770b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3770b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3770b-105">DESCRIPTION</span></span>
<span data-ttu-id="3770b-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會修改 Azure API 管理中的 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="3770b-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="3770b-107">示例</span><span class="sxs-lookup"><span data-stu-id="3770b-107">EXAMPLES</span></span>

### <span data-ttu-id="3770b-108">範例1：變更提供者的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="3770b-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="3770b-109">這個命令會修改具有識別碼 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="3770b-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="3770b-110">此命令會為提供者指定用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="3770b-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="3770b-111">參數</span><span class="sxs-lookup"><span data-stu-id="3770b-111">PARAMETERS</span></span>

### <span data-ttu-id="3770b-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="3770b-112">-ClientId</span></span>
<span data-ttu-id="3770b-113">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="3770b-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="3770b-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3770b-114">-ClientSecret</span></span>
<span data-ttu-id="3770b-115">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="3770b-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="3770b-116">-內容</span><span class="sxs-lookup"><span data-stu-id="3770b-116">-Context</span></span>
<span data-ttu-id="3770b-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="3770b-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3770b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3770b-118">-DefaultProfile</span></span>
<span data-ttu-id="3770b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3770b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3770b-120">-描述</span><span class="sxs-lookup"><span data-stu-id="3770b-120">-Description</span></span>
<span data-ttu-id="3770b-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="3770b-121">Specifies a description.</span></span>

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

### <span data-ttu-id="3770b-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="3770b-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="3770b-123">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="3770b-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="3770b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3770b-124">-Name</span></span>
<span data-ttu-id="3770b-125">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="3770b-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="3770b-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3770b-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3770b-127">指定此 Cmdlet 所修改之提供者的 ID。</span><span class="sxs-lookup"><span data-stu-id="3770b-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="3770b-128">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="3770b-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="3770b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3770b-129">-PassThru</span></span>
<span data-ttu-id="3770b-130">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementOpenIdConnectProvider** 。</span><span class="sxs-lookup"><span data-stu-id="3770b-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3770b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3770b-131">CommonParameters</span></span>
<span data-ttu-id="3770b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3770b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3770b-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3770b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3770b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3770b-134">INPUTS</span></span>

### <span data-ttu-id="3770b-135">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3770b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3770b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="3770b-136">System.String</span></span>

### <span data-ttu-id="3770b-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="3770b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3770b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3770b-138">OUTPUTS</span></span>

### <span data-ttu-id="3770b-139">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3770b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3770b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3770b-140">NOTES</span></span>

## <span data-ttu-id="3770b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3770b-141">RELATED LINKS</span></span>

[<span data-ttu-id="3770b-142">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3770b-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3770b-143">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3770b-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3770b-144">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3770b-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


