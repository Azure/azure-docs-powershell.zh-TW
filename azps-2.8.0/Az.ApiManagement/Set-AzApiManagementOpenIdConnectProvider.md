---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613873"
---
# <span data-ttu-id="26149-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="26149-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="26149-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26149-102">SYNOPSIS</span></span>
<span data-ttu-id="26149-103">修改 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="26149-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="26149-104">句法</span><span class="sxs-lookup"><span data-stu-id="26149-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26149-105">說明</span><span class="sxs-lookup"><span data-stu-id="26149-105">DESCRIPTION</span></span>
<span data-ttu-id="26149-106">**AzApiManagementOpenIdConnectProvider** Cmdlet 會修改 Azure API 管理中的 OpenID connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="26149-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="26149-107">示例</span><span class="sxs-lookup"><span data-stu-id="26149-107">EXAMPLES</span></span>

### <span data-ttu-id="26149-108">範例1：變更提供者的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="26149-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="26149-109">這個命令會修改具有識別碼 OICProvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="26149-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="26149-110">此命令會為提供者指定用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="26149-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="26149-111">參數</span><span class="sxs-lookup"><span data-stu-id="26149-111">PARAMETERS</span></span>

### <span data-ttu-id="26149-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="26149-112">-ClientId</span></span>
<span data-ttu-id="26149-113">指定開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="26149-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="26149-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="26149-114">-ClientSecret</span></span>
<span data-ttu-id="26149-115">指定開發人員主控台的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="26149-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="26149-116">-內容</span><span class="sxs-lookup"><span data-stu-id="26149-116">-Context</span></span>
<span data-ttu-id="26149-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="26149-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26149-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26149-118">-DefaultProfile</span></span>
<span data-ttu-id="26149-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26149-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26149-120">-描述</span><span class="sxs-lookup"><span data-stu-id="26149-120">-Description</span></span>
<span data-ttu-id="26149-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="26149-121">Specifies a description.</span></span>

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

### <span data-ttu-id="26149-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="26149-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="26149-123">指定提供者的中繼資料端點 URI。</span><span class="sxs-lookup"><span data-stu-id="26149-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="26149-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="26149-124">-Name</span></span>
<span data-ttu-id="26149-125">指定提供者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="26149-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="26149-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="26149-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="26149-127">指定此 Cmdlet 所修改之提供者的 ID。</span><span class="sxs-lookup"><span data-stu-id="26149-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="26149-128">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="26149-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="26149-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26149-129">-PassThru</span></span>
<span data-ttu-id="26149-130">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementOpenIdConnectProvider** 。</span><span class="sxs-lookup"><span data-stu-id="26149-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="26149-131">-確認</span><span class="sxs-lookup"><span data-stu-id="26149-131">-Confirm</span></span>
<span data-ttu-id="26149-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26149-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26149-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26149-133">-WhatIf</span></span>
<span data-ttu-id="26149-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26149-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26149-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26149-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26149-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26149-136">CommonParameters</span></span>
<span data-ttu-id="26149-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26149-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26149-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26149-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26149-139">輸入</span><span class="sxs-lookup"><span data-stu-id="26149-139">INPUTS</span></span>

### <span data-ttu-id="26149-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="26149-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26149-141">System.object</span><span class="sxs-lookup"><span data-stu-id="26149-141">System.String</span></span>

### <span data-ttu-id="26149-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="26149-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26149-143">輸出</span><span class="sxs-lookup"><span data-stu-id="26149-143">OUTPUTS</span></span>

### <span data-ttu-id="26149-144">ServiceManagement. PsApiManagementOpenIdConnectProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="26149-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="26149-145">筆記</span><span class="sxs-lookup"><span data-stu-id="26149-145">NOTES</span></span>

## <span data-ttu-id="26149-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="26149-146">RELATED LINKS</span></span>

[<span data-ttu-id="26149-147">AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="26149-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="26149-148">新-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="26149-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="26149-149">移除-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="26149-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


