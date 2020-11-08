---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129707"
---
# <span data-ttu-id="83a99-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="83a99-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="83a99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83a99-102">SYNOPSIS</span></span>
<span data-ttu-id="83a99-103">建立 PsApiManagementSslSetting 的實例</span><span class="sxs-lookup"><span data-stu-id="83a99-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="83a99-104">句法</span><span class="sxs-lookup"><span data-stu-id="83a99-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83a99-105">說明</span><span class="sxs-lookup"><span data-stu-id="83a99-105">DESCRIPTION</span></span>
<span data-ttu-id="83a99-106">[Helper] 命令來建立 PsApiManagementSslSetting 的實例。</span><span class="sxs-lookup"><span data-stu-id="83a99-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="83a99-107">此命令將與 New-AzApiManagement 命令搭配使用。</span><span class="sxs-lookup"><span data-stu-id="83a99-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="83a99-108">示例</span><span class="sxs-lookup"><span data-stu-id="83a99-108">EXAMPLES</span></span>

### <span data-ttu-id="83a99-109">範例1：建立 SSL 設定以在後端和前端啟用 TLS 1。0</span><span class="sxs-lookup"><span data-stu-id="83a99-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="83a99-110">建立新的 PsApiManagementSslSetting 實例，以便在用戶端和 APIM) 與 (閘道之間的 APIM 與後端) 之間的前端 (啟用 TLSv 1.0。</span><span class="sxs-lookup"><span data-stu-id="83a99-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="83a99-111">參數</span><span class="sxs-lookup"><span data-stu-id="83a99-111">PARAMETERS</span></span>

### <span data-ttu-id="83a99-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="83a99-112">-BackendProtocol</span></span>
<span data-ttu-id="83a99-113">後端安全通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="83a99-113">Backend Security protocol settings.</span></span> <span data-ttu-id="83a99-114">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83a99-114">This parameter is optional.</span></span>
<span data-ttu-id="83a99-115">有效的通訊協定設定為 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3。0</span><span class="sxs-lookup"><span data-stu-id="83a99-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="83a99-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="83a99-116">-CipherSuite</span></span>
<span data-ttu-id="83a99-117">以指定順序排列的 Ssl 密碼套件設定。</span><span class="sxs-lookup"><span data-stu-id="83a99-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="83a99-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83a99-118">This parameter is optional.</span></span>
<span data-ttu-id="83a99-119">有效設定為 `TripleDes168` -Enable/Disable Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="83a99-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="83a99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a99-120">-DefaultProfile</span></span>
<span data-ttu-id="83a99-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83a99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83a99-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="83a99-122">-FrontendProtocol</span></span>
<span data-ttu-id="83a99-123">前端安全性協定設定。</span><span class="sxs-lookup"><span data-stu-id="83a99-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="83a99-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83a99-124">This parameter is optional.</span></span>
<span data-ttu-id="83a99-125">有效的通訊協定設定為 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3。0</span><span class="sxs-lookup"><span data-stu-id="83a99-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="83a99-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="83a99-126">-ServerProtocol</span></span>
<span data-ttu-id="83a99-127">伺服器通訊協定設定（例如 Http2）。</span><span class="sxs-lookup"><span data-stu-id="83a99-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="83a99-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83a99-128">This parameter is optional.</span></span>
<span data-ttu-id="83a99-129">有效的設定為 `Http2` -啟用 Http 2。0</span><span class="sxs-lookup"><span data-stu-id="83a99-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="83a99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a99-130">CommonParameters</span></span>
<span data-ttu-id="83a99-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83a99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a99-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83a99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a99-133">輸入</span><span class="sxs-lookup"><span data-stu-id="83a99-133">INPUTS</span></span>

### <span data-ttu-id="83a99-134">所有</span><span class="sxs-lookup"><span data-stu-id="83a99-134">None</span></span>

## <span data-ttu-id="83a99-135">輸出</span><span class="sxs-lookup"><span data-stu-id="83a99-135">OUTPUTS</span></span>

### <span data-ttu-id="83a99-136">PsApiManagementSslSettings 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="83a99-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="83a99-137">筆記</span><span class="sxs-lookup"><span data-stu-id="83a99-137">NOTES</span></span>

## <span data-ttu-id="83a99-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="83a99-138">RELATED LINKS</span></span>

[<span data-ttu-id="83a99-139">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83a99-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

