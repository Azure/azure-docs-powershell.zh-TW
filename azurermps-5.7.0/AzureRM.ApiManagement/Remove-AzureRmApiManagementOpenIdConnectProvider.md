---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454779"
---
# <span data-ttu-id="8a877-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8a877-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="8a877-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a877-102">SYNOPSIS</span></span>
<span data-ttu-id="8a877-103">移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="8a877-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a877-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a877-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a877-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a877-105">DESCRIPTION</span></span>
<span data-ttu-id="8a877-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會針對 Azure API 管理移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="8a877-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="8a877-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a877-107">EXAMPLES</span></span>

### <span data-ttu-id="8a877-108">範例1：移除提供者</span><span class="sxs-lookup"><span data-stu-id="8a877-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="8a877-109">這個命令會移除 ID 為 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="8a877-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="8a877-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a877-110">PARAMETERS</span></span>

### <span data-ttu-id="8a877-111">-內容</span><span class="sxs-lookup"><span data-stu-id="8a877-111">-Context</span></span>
<span data-ttu-id="8a877-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a877-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8a877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a877-113">-DefaultProfile</span></span>
<span data-ttu-id="8a877-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a877-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8a877-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="8a877-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8a877-116">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a877-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a877-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a877-117">-PassThru</span></span>
<span data-ttu-id="8a877-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="8a877-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="8a877-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8a877-119">-Confirm</span></span>
<span data-ttu-id="8a877-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a877-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a877-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a877-121">-WhatIf</span></span>
<span data-ttu-id="8a877-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a877-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a877-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a877-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a877-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a877-124">CommonParameters</span></span>
<span data-ttu-id="8a877-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a877-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a877-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a877-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a877-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8a877-127">INPUTS</span></span>

### <span data-ttu-id="8a877-128">所有</span><span class="sxs-lookup"><span data-stu-id="8a877-128">None</span></span>
<span data-ttu-id="8a877-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8a877-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a877-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8a877-130">OUTPUTS</span></span>

### <span data-ttu-id="8a877-131">布林值</span><span class="sxs-lookup"><span data-stu-id="8a877-131">Boolean</span></span>

## <span data-ttu-id="8a877-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8a877-132">NOTES</span></span>

## <span data-ttu-id="8a877-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a877-133">RELATED LINKS</span></span>

[<span data-ttu-id="8a877-134">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8a877-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8a877-135">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8a877-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8a877-136">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8a877-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


