---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613965"
---
# <span data-ttu-id="ae22d-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="ae22d-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="ae22d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae22d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae22d-103">建立 PsApiManagementSslSetting 的實例</span><span class="sxs-lookup"><span data-stu-id="ae22d-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="ae22d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae22d-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae22d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae22d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae22d-106">[Helper] 命令來建立 PsApiManagementSslSetting 的實例。</span><span class="sxs-lookup"><span data-stu-id="ae22d-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="ae22d-107">此命令將與 New-AzApiManagement 命令搭配使用。</span><span class="sxs-lookup"><span data-stu-id="ae22d-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="ae22d-108">示例</span><span class="sxs-lookup"><span data-stu-id="ae22d-108">EXAMPLES</span></span>

### <span data-ttu-id="ae22d-109">範例1：建立 SSL 設定以在後端和前端啟用 TLS 1。0</span><span class="sxs-lookup"><span data-stu-id="ae22d-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="ae22d-110">建立新的 PsApiManagementSslSetting 實例，以便在用戶端和 APIM) 與 (閘道之間的 APIM 與後端) 之間的前端 (啟用 TLSv 1.0。</span><span class="sxs-lookup"><span data-stu-id="ae22d-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="ae22d-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae22d-111">PARAMETERS</span></span>

### <span data-ttu-id="ae22d-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="ae22d-112">-BackendProtocol</span></span>
<span data-ttu-id="ae22d-113">後端安全通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="ae22d-113">Backend Security protocol settings.</span></span> <span data-ttu-id="ae22d-114">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae22d-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae22d-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ae22d-115">-CipherSuite</span></span>
<span data-ttu-id="ae22d-116">以指定順序排列的 Ssl 密碼套件設定。</span><span class="sxs-lookup"><span data-stu-id="ae22d-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="ae22d-117">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae22d-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae22d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae22d-118">-DefaultProfile</span></span>
<span data-ttu-id="ae22d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae22d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae22d-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="ae22d-120">-FrontendProtocol</span></span>
<span data-ttu-id="ae22d-121">前端安全性協定設定。</span><span class="sxs-lookup"><span data-stu-id="ae22d-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="ae22d-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae22d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae22d-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="ae22d-123">-ServerProtocol</span></span>
<span data-ttu-id="ae22d-124">伺服器通訊協定設定（例如 Http2）。</span><span class="sxs-lookup"><span data-stu-id="ae22d-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="ae22d-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ae22d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae22d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae22d-126">CommonParameters</span></span>
<span data-ttu-id="ae22d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae22d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae22d-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae22d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae22d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ae22d-129">INPUTS</span></span>

### <span data-ttu-id="ae22d-130">所有</span><span class="sxs-lookup"><span data-stu-id="ae22d-130">None</span></span>

## <span data-ttu-id="ae22d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ae22d-131">OUTPUTS</span></span>

### <span data-ttu-id="ae22d-132">PsApiManagementSslSettings 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="ae22d-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="ae22d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ae22d-133">NOTES</span></span>

## <span data-ttu-id="ae22d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae22d-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae22d-135">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ae22d-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

