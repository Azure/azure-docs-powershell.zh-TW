---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136086"
---
# <span data-ttu-id="2b6ed-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b6ed-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2b6ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6ed-103">取得現有閘道的全部或特定主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2b6ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b6ed-104">SYNTAX</span></span>

### <span data-ttu-id="2b6ed-105">GetByGatewayId (預設) </span><span class="sxs-lookup"><span data-stu-id="2b6ed-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6ed-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="2b6ed-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b6ed-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b6ed-107">DESCRIPTION</span></span>
<span data-ttu-id="2b6ed-108">**AzApiManagementGatewayHostnameConfiguration** Cmdlet 會取得現有閘道的所有或特定主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="2b6ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b6ed-109">EXAMPLES</span></span>

### <span data-ttu-id="2b6ed-110">範例1：取得閘道的所有主機名稱設定</span><span class="sxs-lookup"><span data-stu-id="2b6ed-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="2b6ed-111">這個命令會取得「0123456789」閘道的所有主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="2b6ed-112">範例2：取得閘道的主機名稱設定</span><span class="sxs-lookup"><span data-stu-id="2b6ed-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="2b6ed-113">這個命令會針對 "0123456789" 閘道取得 "123" 主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="2b6ed-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b6ed-114">PARAMETERS</span></span>

### <span data-ttu-id="2b6ed-115">-內容</span><span class="sxs-lookup"><span data-stu-id="2b6ed-115">-Context</span></span>
<span data-ttu-id="2b6ed-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b6ed-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2b6ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6ed-118">-DefaultProfile</span></span>
<span data-ttu-id="2b6ed-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b6ed-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2b6ed-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="2b6ed-121">主機名稱配置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="2b6ed-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6ed-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2b6ed-123">-GatewayId</span></span>
<span data-ttu-id="2b6ed-124">閘道識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-124">Gateway identifier.</span></span>
<span data-ttu-id="2b6ed-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-125">This parameter is required.</span></span>

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

### <span data-ttu-id="2b6ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6ed-126">CommonParameters</span></span>
<span data-ttu-id="2b6ed-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6ed-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b6ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6ed-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2b6ed-129">INPUTS</span></span>

### <span data-ttu-id="2b6ed-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2b6ed-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b6ed-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2b6ed-131">System.String</span></span>

## <span data-ttu-id="2b6ed-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2b6ed-132">OUTPUTS</span></span>

### <span data-ttu-id="2b6ed-133">ServiceManagement. PsApiManagementGatewayHostnameConfiguration （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2b6ed-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="2b6ed-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2b6ed-134">NOTES</span></span>

## <span data-ttu-id="2b6ed-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b6ed-135">RELATED LINKS</span></span>