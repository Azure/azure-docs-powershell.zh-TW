---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450915"
---
# <span data-ttu-id="045f6-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="045f6-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="045f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="045f6-102">SYNOPSIS</span></span>
<span data-ttu-id="045f6-103">修改 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="045f6-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="045f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="045f6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="045f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="045f6-105">DESCRIPTION</span></span>
<span data-ttu-id="045f6-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會修改 Azure API 管理中的 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="045f6-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="045f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="045f6-107">EXAMPLES</span></span>

### <span data-ttu-id="045f6-108">範例1：變更提供者的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="045f6-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="045f6-109">這個命令會修改具有識別碼 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="045f6-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="045f6-110">此命令會為提供者指定用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="045f6-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="045f6-111">參數</span><span class="sxs-lookup"><span data-stu-id="045f6-111">PARAMETERS</span></span>

### <span data-ttu-id="045f6-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="045f6-112">-ClientId</span></span>
<span data-ttu-id="045f6-113">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="045f6-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="045f6-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="045f6-114">-ClientSecret</span></span>
<span data-ttu-id="045f6-115">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="045f6-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="045f6-116">-內容</span><span class="sxs-lookup"><span data-stu-id="045f6-116">-Context</span></span>
<span data-ttu-id="045f6-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="045f6-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="045f6-118">-描述</span><span class="sxs-lookup"><span data-stu-id="045f6-118">-Description</span></span>
<span data-ttu-id="045f6-119">指定描述。</span><span class="sxs-lookup"><span data-stu-id="045f6-119">Specifies a description.</span></span>

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

### <span data-ttu-id="045f6-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="045f6-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="045f6-121">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="045f6-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="045f6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="045f6-122">-Name</span></span>
<span data-ttu-id="045f6-123">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="045f6-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="045f6-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="045f6-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="045f6-125">指定此 Cmdlet 所修改之提供者的 ID。</span><span class="sxs-lookup"><span data-stu-id="045f6-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="045f6-126">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="045f6-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="045f6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="045f6-127">-PassThru</span></span>
<span data-ttu-id="045f6-128">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementOpenIdConnectProvider** 。</span><span class="sxs-lookup"><span data-stu-id="045f6-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="045f6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045f6-129">-DefaultProfile</span></span>
<span data-ttu-id="045f6-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="045f6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="045f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045f6-131">CommonParameters</span></span>
<span data-ttu-id="045f6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="045f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045f6-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="045f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045f6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="045f6-134">INPUTS</span></span>

## <span data-ttu-id="045f6-135">輸出</span><span class="sxs-lookup"><span data-stu-id="045f6-135">OUTPUTS</span></span>

### <span data-ttu-id="045f6-136">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="045f6-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="045f6-137">筆記</span><span class="sxs-lookup"><span data-stu-id="045f6-137">NOTES</span></span>

## <span data-ttu-id="045f6-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="045f6-138">RELATED LINKS</span></span>

[<span data-ttu-id="045f6-139">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="045f6-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="045f6-140">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="045f6-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="045f6-141">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="045f6-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


