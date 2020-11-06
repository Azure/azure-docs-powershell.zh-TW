---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452559"
---
# <span data-ttu-id="3dce0-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3dce0-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="3dce0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dce0-102">SYNOPSIS</span></span>
<span data-ttu-id="3dce0-103">將內容載入到端點。</span><span class="sxs-lookup"><span data-stu-id="3dce0-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dce0-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dce0-104">SYNTAX</span></span>

### <span data-ttu-id="3dce0-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="3dce0-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dce0-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="3dce0-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dce0-107">說明</span><span class="sxs-lookup"><span data-stu-id="3dce0-107">DESCRIPTION</span></span>
<span data-ttu-id="3dce0-108">**AzureRmCdnEndpointContent** Cmdlet 會從來源伺服器載入 Azure 內容傳遞網路 (CDN) 端點的內容。</span><span class="sxs-lookup"><span data-stu-id="3dce0-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3dce0-109">示例</span><span class="sxs-lookup"><span data-stu-id="3dce0-109">EXAMPLES</span></span>

## <span data-ttu-id="3dce0-110">參數</span><span class="sxs-lookup"><span data-stu-id="3dce0-110">PARAMETERS</span></span>

### <span data-ttu-id="3dce0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dce0-111">-CdnEndpoint</span></span>
<span data-ttu-id="3dce0-112">Sepcifies CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="3dce0-112">Sepcifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dce0-113">-終結點</span><span class="sxs-lookup"><span data-stu-id="3dce0-113">-EndpointName</span></span>
<span data-ttu-id="3dce0-114">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dce0-114">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dce0-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="3dce0-115">-LoadContent</span></span>
<span data-ttu-id="3dce0-116">指定此 Cmdlet 發佈之原始伺服器內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="3dce0-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dce0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dce0-117">-PassThru</span></span>
<span data-ttu-id="3dce0-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3dce0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3dce0-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3dce0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3dce0-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3dce0-120">-ProfileName</span></span>
<span data-ttu-id="3dce0-121">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dce0-121">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dce0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dce0-122">-ResourceGroupName</span></span>
<span data-ttu-id="3dce0-123">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dce0-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dce0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dce0-124">-DefaultProfile</span></span>
<span data-ttu-id="3dce0-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dce0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dce0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dce0-126">CommonParameters</span></span>
<span data-ttu-id="3dce0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dce0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dce0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dce0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dce0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3dce0-129">INPUTS</span></span>

### <span data-ttu-id="3dce0-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dce0-130">PSEndpoint</span></span>
<span data-ttu-id="3dce0-131">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3dce0-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3dce0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3dce0-132">OUTPUTS</span></span>

### <span data-ttu-id="3dce0-133">System.object</span><span class="sxs-lookup"><span data-stu-id="3dce0-133">System.Boolean</span></span>

## <span data-ttu-id="3dce0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3dce0-134">NOTES</span></span>

## <span data-ttu-id="3dce0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dce0-135">RELATED LINKS</span></span>

[<span data-ttu-id="3dce0-136">取消發佈-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3dce0-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


