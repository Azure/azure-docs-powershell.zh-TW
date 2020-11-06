---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2ce3863a546af0f8c9da3c37a75b540d2a859da1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614002"
---
# <span data-ttu-id="0709b-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0709b-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="0709b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0709b-102">SYNOPSIS</span></span>
<span data-ttu-id="0709b-103">建立新的後端 Proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="0709b-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="0709b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0709b-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0709b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0709b-105">DESCRIPTION</span></span>
<span data-ttu-id="0709b-106">建立新的後端 Proxy 物件，可在建立新的後端實體時進行管道。</span><span class="sxs-lookup"><span data-stu-id="0709b-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="0709b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0709b-107">EXAMPLES</span></span>

### <span data-ttu-id="0709b-108">建立後端 Proxy In-Memory 物件</span><span class="sxs-lookup"><span data-stu-id="0709b-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="0709b-109">建立後端 Proxy 物件並設定後端</span><span class="sxs-lookup"><span data-stu-id="0709b-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="0709b-110">參數</span><span class="sxs-lookup"><span data-stu-id="0709b-110">PARAMETERS</span></span>

### <span data-ttu-id="0709b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0709b-111">-DefaultProfile</span></span>
<span data-ttu-id="0709b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0709b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0709b-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="0709b-113">-ProxyCredential</span></span>
<span data-ttu-id="0709b-114">用來連接到後端 Proxy 的認證。</span><span class="sxs-lookup"><span data-stu-id="0709b-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="0709b-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0709b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="0709b-116">-Url</span><span class="sxs-lookup"><span data-stu-id="0709b-116">-Url</span></span>
<span data-ttu-id="0709b-117">將來電轉接到後端時要使用之 Proxy 伺服器的 Url。</span><span class="sxs-lookup"><span data-stu-id="0709b-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="0709b-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0709b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0709b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0709b-119">CommonParameters</span></span>
<span data-ttu-id="0709b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0709b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0709b-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0709b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0709b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0709b-122">INPUTS</span></span>

### <span data-ttu-id="0709b-123">所有</span><span class="sxs-lookup"><span data-stu-id="0709b-123">None</span></span>

## <span data-ttu-id="0709b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0709b-124">OUTPUTS</span></span>

### <span data-ttu-id="0709b-125">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0709b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="0709b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0709b-126">NOTES</span></span>

## <span data-ttu-id="0709b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0709b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0709b-128">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0709b-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="0709b-129">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0709b-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="0709b-130">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0709b-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="0709b-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0709b-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="0709b-132">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0709b-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
