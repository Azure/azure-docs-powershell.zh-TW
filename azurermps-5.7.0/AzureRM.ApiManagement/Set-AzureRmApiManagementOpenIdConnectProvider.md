---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456263"
---
# <span data-ttu-id="4296f-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4296f-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4296f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4296f-102">SYNOPSIS</span></span>
<span data-ttu-id="4296f-103">修改 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="4296f-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4296f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4296f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4296f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4296f-105">DESCRIPTION</span></span>
<span data-ttu-id="4296f-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會修改 Azure API 管理中的 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="4296f-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="4296f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4296f-107">EXAMPLES</span></span>

### <span data-ttu-id="4296f-108">範例1：變更提供者的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="4296f-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="4296f-109">這個命令會修改具有識別碼 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="4296f-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="4296f-110">此命令會為提供者指定用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="4296f-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="4296f-111">參數</span><span class="sxs-lookup"><span data-stu-id="4296f-111">PARAMETERS</span></span>

### <span data-ttu-id="4296f-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4296f-112">-ClientId</span></span>
<span data-ttu-id="4296f-113">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="4296f-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="4296f-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4296f-114">-ClientSecret</span></span>
<span data-ttu-id="4296f-115">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="4296f-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="4296f-116">-內容</span><span class="sxs-lookup"><span data-stu-id="4296f-116">-Context</span></span>
<span data-ttu-id="4296f-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4296f-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4296f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4296f-118">-DefaultProfile</span></span>
<span data-ttu-id="4296f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4296f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4296f-120">-描述</span><span class="sxs-lookup"><span data-stu-id="4296f-120">-Description</span></span>
<span data-ttu-id="4296f-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="4296f-121">Specifies a description.</span></span>

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

### <span data-ttu-id="4296f-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="4296f-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="4296f-123">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="4296f-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="4296f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4296f-124">-Name</span></span>
<span data-ttu-id="4296f-125">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4296f-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="4296f-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4296f-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4296f-127">指定此 Cmdlet 所修改之提供者的 ID。</span><span class="sxs-lookup"><span data-stu-id="4296f-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="4296f-128">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="4296f-128">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4296f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4296f-129">-PassThru</span></span>
<span data-ttu-id="4296f-130">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementOpenIdConnectProvider** 。</span><span class="sxs-lookup"><span data-stu-id="4296f-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4296f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4296f-131">CommonParameters</span></span>
<span data-ttu-id="4296f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4296f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4296f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4296f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4296f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4296f-134">INPUTS</span></span>

### <span data-ttu-id="4296f-135">所有</span><span class="sxs-lookup"><span data-stu-id="4296f-135">None</span></span>
<span data-ttu-id="4296f-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4296f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4296f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4296f-137">OUTPUTS</span></span>

### <span data-ttu-id="4296f-138">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4296f-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4296f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4296f-139">NOTES</span></span>

## <span data-ttu-id="4296f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4296f-140">RELATED LINKS</span></span>

[<span data-ttu-id="4296f-141">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4296f-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4296f-142">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4296f-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4296f-143">移除-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4296f-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


