---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450110"
---
# <span data-ttu-id="80205-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="80205-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="80205-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80205-102">SYNOPSIS</span></span>
<span data-ttu-id="80205-103">建立新的後端 Proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="80205-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80205-104">句法</span><span class="sxs-lookup"><span data-stu-id="80205-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80205-105">說明</span><span class="sxs-lookup"><span data-stu-id="80205-105">DESCRIPTION</span></span>
<span data-ttu-id="80205-106">建立新的後端 Proxy 物件，可在建立新的後端實體時進行管道。</span><span class="sxs-lookup"><span data-stu-id="80205-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="80205-107">示例</span><span class="sxs-lookup"><span data-stu-id="80205-107">EXAMPLES</span></span>

### <span data-ttu-id="80205-108">建立後端 Proxy In-Memory 物件</span><span class="sxs-lookup"><span data-stu-id="80205-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="80205-109">建立後端 Proxy 物件</span><span class="sxs-lookup"><span data-stu-id="80205-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="80205-110">參數</span><span class="sxs-lookup"><span data-stu-id="80205-110">PARAMETERS</span></span>

### <span data-ttu-id="80205-111">-Password</span><span class="sxs-lookup"><span data-stu-id="80205-111">-Password</span></span>
<span data-ttu-id="80205-112">用來連接後端 Proxy 的 Proxy 密碼。</span><span class="sxs-lookup"><span data-stu-id="80205-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="80205-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="80205-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80205-114">-Url</span><span class="sxs-lookup"><span data-stu-id="80205-114">-Url</span></span>
<span data-ttu-id="80205-115">將來電轉接到後端時要使用之 Proxy 伺服器的 Url。</span><span class="sxs-lookup"><span data-stu-id="80205-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="80205-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="80205-116">This parameter is required.</span></span>

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

### <span data-ttu-id="80205-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="80205-117">-UserName</span></span>
<span data-ttu-id="80205-118">用來連接後端 Proxy 的 Proxy 使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="80205-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="80205-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="80205-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80205-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80205-120">-DefaultProfile</span></span>
<span data-ttu-id="80205-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80205-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80205-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80205-122">CommonParameters</span></span>
<span data-ttu-id="80205-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80205-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80205-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80205-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80205-125">輸入</span><span class="sxs-lookup"><span data-stu-id="80205-125">INPUTS</span></span>

## <span data-ttu-id="80205-126">輸出</span><span class="sxs-lookup"><span data-stu-id="80205-126">OUTPUTS</span></span>

### <span data-ttu-id="80205-127">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="80205-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="80205-128">筆記</span><span class="sxs-lookup"><span data-stu-id="80205-128">NOTES</span></span>

## <span data-ttu-id="80205-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="80205-129">RELATED LINKS</span></span>

[<span data-ttu-id="80205-130">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80205-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="80205-131">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80205-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="80205-132">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="80205-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="80205-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80205-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="80205-134">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="80205-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
