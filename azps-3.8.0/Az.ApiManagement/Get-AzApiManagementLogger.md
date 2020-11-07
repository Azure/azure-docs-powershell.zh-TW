---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957116"
---
# <span data-ttu-id="13108-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="13108-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="13108-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13108-102">SYNOPSIS</span></span>
<span data-ttu-id="13108-103">取得 API 記錄管理器物件。</span><span class="sxs-lookup"><span data-stu-id="13108-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="13108-104">句法</span><span class="sxs-lookup"><span data-stu-id="13108-104">SYNTAX</span></span>

### <span data-ttu-id="13108-105">GetAllLoggers (預設) </span><span class="sxs-lookup"><span data-stu-id="13108-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13108-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="13108-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13108-107">說明</span><span class="sxs-lookup"><span data-stu-id="13108-107">DESCRIPTION</span></span>
<span data-ttu-id="13108-108">**AzApiManagementLogger** Cmdlet 會取得 Azure API 管理 **記錄器** 或所有的記錄器。</span><span class="sxs-lookup"><span data-stu-id="13108-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="13108-109">示例</span><span class="sxs-lookup"><span data-stu-id="13108-109">EXAMPLES</span></span>

### <span data-ttu-id="13108-110">範例1：取得所有的記錄器</span><span class="sxs-lookup"><span data-stu-id="13108-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="13108-111">這個命令會取得指定內容的所有記錄器。</span><span class="sxs-lookup"><span data-stu-id="13108-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="13108-112">範例2：取得特定的記錄器</span><span class="sxs-lookup"><span data-stu-id="13108-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="13108-113">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="13108-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="13108-114">參數</span><span class="sxs-lookup"><span data-stu-id="13108-114">PARAMETERS</span></span>

### <span data-ttu-id="13108-115">-內容</span><span class="sxs-lookup"><span data-stu-id="13108-115">-Context</span></span>
<span data-ttu-id="13108-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="13108-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13108-117">-DefaultProfile</span></span>
<span data-ttu-id="13108-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13108-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13108-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="13108-119">-LoggerId</span></span>
<span data-ttu-id="13108-120">指定要取得的特定記錄器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="13108-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13108-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13108-121">CommonParameters</span></span>
<span data-ttu-id="13108-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13108-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13108-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13108-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13108-124">輸入</span><span class="sxs-lookup"><span data-stu-id="13108-124">INPUTS</span></span>

### <span data-ttu-id="13108-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="13108-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="13108-126">System.object</span><span class="sxs-lookup"><span data-stu-id="13108-126">System.String</span></span>

## <span data-ttu-id="13108-127">輸出</span><span class="sxs-lookup"><span data-stu-id="13108-127">OUTPUTS</span></span>

### <span data-ttu-id="13108-128">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="13108-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="13108-129">筆記</span><span class="sxs-lookup"><span data-stu-id="13108-129">NOTES</span></span>

## <span data-ttu-id="13108-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="13108-130">RELATED LINKS</span></span>

[<span data-ttu-id="13108-131">新-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="13108-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="13108-132">移除-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="13108-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="13108-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="13108-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


