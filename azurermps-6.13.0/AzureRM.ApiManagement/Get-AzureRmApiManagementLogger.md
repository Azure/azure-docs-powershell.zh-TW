---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: ee293fcedd6f52f8fee8f14a207862c3b9a11d11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444180"
---
# <span data-ttu-id="9545c-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9545c-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="9545c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9545c-102">SYNOPSIS</span></span>
<span data-ttu-id="9545c-103">取得 API 記錄管理器物件。</span><span class="sxs-lookup"><span data-stu-id="9545c-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9545c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9545c-104">SYNTAX</span></span>

### <span data-ttu-id="9545c-105">GetAllLoggers (預設) </span><span class="sxs-lookup"><span data-stu-id="9545c-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9545c-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="9545c-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9545c-107">說明</span><span class="sxs-lookup"><span data-stu-id="9545c-107">DESCRIPTION</span></span>
<span data-ttu-id="9545c-108">**AzureRmApiManagementLogger** Cmdlet 會取得 Azure API 管理 **記錄器** 或所有的記錄器。</span><span class="sxs-lookup"><span data-stu-id="9545c-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="9545c-109">示例</span><span class="sxs-lookup"><span data-stu-id="9545c-109">EXAMPLES</span></span>

### <span data-ttu-id="9545c-110">範例1：取得所有的記錄器</span><span class="sxs-lookup"><span data-stu-id="9545c-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="9545c-111">這個命令會取得指定內容的所有記錄器。</span><span class="sxs-lookup"><span data-stu-id="9545c-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="9545c-112">範例2：取得特定的記錄器</span><span class="sxs-lookup"><span data-stu-id="9545c-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="9545c-113">這個命令會移除 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="9545c-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="9545c-114">參數</span><span class="sxs-lookup"><span data-stu-id="9545c-114">PARAMETERS</span></span>

### <span data-ttu-id="9545c-115">-內容</span><span class="sxs-lookup"><span data-stu-id="9545c-115">-Context</span></span>
<span data-ttu-id="9545c-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9545c-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9545c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9545c-117">-DefaultProfile</span></span>
<span data-ttu-id="9545c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9545c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9545c-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="9545c-119">-LoggerId</span></span>
<span data-ttu-id="9545c-120">指定要取得的特定記錄器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9545c-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="9545c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9545c-121">CommonParameters</span></span>
<span data-ttu-id="9545c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9545c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9545c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9545c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9545c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9545c-124">INPUTS</span></span>

### <span data-ttu-id="9545c-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9545c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9545c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="9545c-126">System.String</span></span>

## <span data-ttu-id="9545c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9545c-127">OUTPUTS</span></span>

### <span data-ttu-id="9545c-128">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9545c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="9545c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9545c-129">NOTES</span></span>

## <span data-ttu-id="9545c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9545c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9545c-131">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9545c-131">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="9545c-132">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9545c-132">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="9545c-133">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="9545c-133">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


