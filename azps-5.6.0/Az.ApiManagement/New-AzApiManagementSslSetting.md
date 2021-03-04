---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914953"
---
# <span data-ttu-id="33d44-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="33d44-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="33d44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33d44-102">SYNOPSIS</span></span>
<span data-ttu-id="33d44-103">建立 PsApiManagementSslSetting 的實例</span><span class="sxs-lookup"><span data-stu-id="33d44-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="33d44-104">語法</span><span class="sxs-lookup"><span data-stu-id="33d44-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33d44-105">描述</span><span class="sxs-lookup"><span data-stu-id="33d44-105">DESCRIPTION</span></span>
<span data-ttu-id="33d44-106">建立 PsApiManagementSslSetting 實例的協助程式命令。</span><span class="sxs-lookup"><span data-stu-id="33d44-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="33d44-107">此命令會與命令一New-AzApiManagement使用。</span><span class="sxs-lookup"><span data-stu-id="33d44-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="33d44-108">例子</span><span class="sxs-lookup"><span data-stu-id="33d44-108">EXAMPLES</span></span>

### <span data-ttu-id="33d44-109">範例 1：建立 SSL 設定以在後端和 Frontend 上啟用 TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="33d44-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="33d44-110">在 ApiManagement 閘道的 APIM 與後端) 之間，在用戶端和 APIM) 與後端 (之間的 Frontend (中，建立 PsApiManagementSslSetting 的新實例以啟用 TLSv 1.0。</span><span class="sxs-lookup"><span data-stu-id="33d44-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="33d44-111">參數</span><span class="sxs-lookup"><span data-stu-id="33d44-111">PARAMETERS</span></span>

### <span data-ttu-id="33d44-112">-後端Protocol</span><span class="sxs-lookup"><span data-stu-id="33d44-112">-BackendProtocol</span></span>
<span data-ttu-id="33d44-113">後端安全性通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="33d44-113">Backend Security protocol settings.</span></span> <span data-ttu-id="33d44-114">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="33d44-114">This parameter is optional.</span></span>
<span data-ttu-id="33d44-115">有效的通訊協定設定 `Tls11` 為 - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="33d44-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d44-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="33d44-116">-CipherSuite</span></span>
<span data-ttu-id="33d44-117">以指定的順序設定 Ssl 密碼套件。</span><span class="sxs-lookup"><span data-stu-id="33d44-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="33d44-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="33d44-118">This parameter is optional.</span></span>
<span data-ttu-id="33d44-119">有效的設定為 `TripleDes168` - 啟用/停用 Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="33d44-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d44-120">-DefaultProfile</span></span>
<span data-ttu-id="33d44-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33d44-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d44-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="33d44-122">-FrontendProtocol</span></span>
<span data-ttu-id="33d44-123">Frontend 安全性通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="33d44-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="33d44-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="33d44-124">This parameter is optional.</span></span>
<span data-ttu-id="33d44-125">有效的通訊協定設定 `Tls11` 為 - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="33d44-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d44-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="33d44-126">-ServerProtocol</span></span>
<span data-ttu-id="33d44-127">伺服器通訊協定設定，例如 HTTP2。</span><span class="sxs-lookup"><span data-stu-id="33d44-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="33d44-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="33d44-128">This parameter is optional.</span></span>
<span data-ttu-id="33d44-129">有效的設定 `Http2` - 啟用 HTTP 2.0</span><span class="sxs-lookup"><span data-stu-id="33d44-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d44-130">CommonParameters</span></span>
<span data-ttu-id="33d44-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33d44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d44-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33d44-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d44-133">輸入</span><span class="sxs-lookup"><span data-stu-id="33d44-133">INPUTS</span></span>

### <span data-ttu-id="33d44-134">沒有</span><span class="sxs-lookup"><span data-stu-id="33d44-134">None</span></span>

## <span data-ttu-id="33d44-135">輸出</span><span class="sxs-lookup"><span data-stu-id="33d44-135">OUTPUTS</span></span>

### <span data-ttu-id="33d44-136">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="33d44-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="33d44-137">筆記</span><span class="sxs-lookup"><span data-stu-id="33d44-137">NOTES</span></span>

## <span data-ttu-id="33d44-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="33d44-138">RELATED LINKS</span></span>

[<span data-ttu-id="33d44-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="33d44-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

