---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2230785968fd0e2d84587914641390306948bef4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410645"
---
# <span data-ttu-id="7d01a-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7d01a-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="7d01a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d01a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d01a-103">建立新的後端 Proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="7d01a-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="7d01a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d01a-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d01a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d01a-105">DESCRIPTION</span></span>
<span data-ttu-id="7d01a-106">建立新後端 Proxy 物件，可在建立新後端實體時進行管道處理。</span><span class="sxs-lookup"><span data-stu-id="7d01a-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="7d01a-107">例子</span><span class="sxs-lookup"><span data-stu-id="7d01a-107">EXAMPLES</span></span>

### <span data-ttu-id="7d01a-108">建立後端 Proxy In-Memory物件</span><span class="sxs-lookup"><span data-stu-id="7d01a-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="7d01a-109">建立後端 Proxy 物件並設定後端</span><span class="sxs-lookup"><span data-stu-id="7d01a-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="7d01a-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d01a-110">PARAMETERS</span></span>

### <span data-ttu-id="7d01a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d01a-111">-DefaultProfile</span></span>
<span data-ttu-id="7d01a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d01a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d01a-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="7d01a-113">-ProxyCredential</span></span>
<span data-ttu-id="7d01a-114">用來連接至後端 Proxy 的認證。</span><span class="sxs-lookup"><span data-stu-id="7d01a-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="7d01a-115">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="7d01a-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d01a-116">-Url</span><span class="sxs-lookup"><span data-stu-id="7d01a-116">-Url</span></span>
<span data-ttu-id="7d01a-117">將呼叫轉往後端時所使用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="7d01a-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="7d01a-118">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="7d01a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7d01a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d01a-119">CommonParameters</span></span>
<span data-ttu-id="7d01a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d01a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d01a-121">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d01a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d01a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7d01a-122">INPUTS</span></span>

### <span data-ttu-id="7d01a-123">沒有</span><span class="sxs-lookup"><span data-stu-id="7d01a-123">None</span></span>

## <span data-ttu-id="7d01a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7d01a-124">OUTPUTS</span></span>

### <span data-ttu-id="7d01a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7d01a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="7d01a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7d01a-126">NOTES</span></span>

## <span data-ttu-id="7d01a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d01a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7d01a-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d01a-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="7d01a-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d01a-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="7d01a-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7d01a-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7d01a-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d01a-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7d01a-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d01a-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
