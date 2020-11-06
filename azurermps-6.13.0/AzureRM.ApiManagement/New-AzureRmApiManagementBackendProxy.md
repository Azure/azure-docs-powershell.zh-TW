---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447523"
---
# <span data-ttu-id="e368a-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e368a-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="e368a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e368a-102">SYNOPSIS</span></span>
<span data-ttu-id="e368a-103">建立新的後端 Proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="e368a-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e368a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e368a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e368a-105">說明</span><span class="sxs-lookup"><span data-stu-id="e368a-105">DESCRIPTION</span></span>
<span data-ttu-id="e368a-106">建立新的後端 Proxy 物件，可在建立新的後端實體時進行管道。</span><span class="sxs-lookup"><span data-stu-id="e368a-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="e368a-107">示例</span><span class="sxs-lookup"><span data-stu-id="e368a-107">EXAMPLES</span></span>

### <span data-ttu-id="e368a-108">建立後端 Proxy In-Memory 物件</span><span class="sxs-lookup"><span data-stu-id="e368a-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="e368a-109">建立後端 Proxy 物件並設定後端</span><span class="sxs-lookup"><span data-stu-id="e368a-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="e368a-110">參數</span><span class="sxs-lookup"><span data-stu-id="e368a-110">PARAMETERS</span></span>

### <span data-ttu-id="e368a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e368a-111">-DefaultProfile</span></span>
<span data-ttu-id="e368a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e368a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e368a-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="e368a-113">-ProxyCredential</span></span>
<span data-ttu-id="e368a-114">用來連接到後端 Proxy 的認證。</span><span class="sxs-lookup"><span data-stu-id="e368a-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="e368a-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e368a-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e368a-116">-Url</span><span class="sxs-lookup"><span data-stu-id="e368a-116">-Url</span></span>
<span data-ttu-id="e368a-117">將來電轉接到後端時要使用之 Proxy 伺服器的 Url。</span><span class="sxs-lookup"><span data-stu-id="e368a-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="e368a-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e368a-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e368a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e368a-119">CommonParameters</span></span>
<span data-ttu-id="e368a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e368a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e368a-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e368a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e368a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e368a-122">INPUTS</span></span>

### <span data-ttu-id="e368a-123">所有</span><span class="sxs-lookup"><span data-stu-id="e368a-123">None</span></span>

## <span data-ttu-id="e368a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e368a-124">OUTPUTS</span></span>

### <span data-ttu-id="e368a-125">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e368a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="e368a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e368a-126">NOTES</span></span>

## <span data-ttu-id="e368a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e368a-127">RELATED LINKS</span></span>

[<span data-ttu-id="e368a-128">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e368a-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e368a-129">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e368a-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e368a-130">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e368a-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e368a-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e368a-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e368a-132">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e368a-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
