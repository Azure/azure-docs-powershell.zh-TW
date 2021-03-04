---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907174"
---
# <span data-ttu-id="0f503-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0f503-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="0f503-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f503-102">SYNOPSIS</span></span>
<span data-ttu-id="0f503-103">獲得 API 記錄管理器物件。</span><span class="sxs-lookup"><span data-stu-id="0f503-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="0f503-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f503-104">SYNTAX</span></span>

### <span data-ttu-id="0f503-105">GetAllLo用 (預設) </span><span class="sxs-lookup"><span data-stu-id="0f503-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f503-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="0f503-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f503-107">描述</span><span class="sxs-lookup"><span data-stu-id="0f503-107">DESCRIPTION</span></span>
<span data-ttu-id="0f503-108">**Get-AzApiManagementLoagementLodlet** 會取得 Azure API 管理 **記錄器** 或所有記錄器。</span><span class="sxs-lookup"><span data-stu-id="0f503-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="0f503-109">例子</span><span class="sxs-lookup"><span data-stu-id="0f503-109">EXAMPLES</span></span>

### <span data-ttu-id="0f503-110">範例 1：取得所有記錄器</span><span class="sxs-lookup"><span data-stu-id="0f503-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="0f503-111">此命令會針對指定的上下文獲得所有記錄器。</span><span class="sxs-lookup"><span data-stu-id="0f503-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="0f503-112">範例 2：取得特定的記錄器</span><span class="sxs-lookup"><span data-stu-id="0f503-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="0f503-113">此命令會移除具有識別碼記錄器123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="0f503-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0f503-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f503-114">PARAMETERS</span></span>

### <span data-ttu-id="0f503-115">-內容</span><span class="sxs-lookup"><span data-stu-id="0f503-115">-Context</span></span>
<span data-ttu-id="0f503-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0f503-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0f503-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f503-117">-DefaultProfile</span></span>
<span data-ttu-id="0f503-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f503-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f503-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="0f503-119">-LoggerId</span></span>
<span data-ttu-id="0f503-120">指定要取得的特定記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f503-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="0f503-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f503-121">CommonParameters</span></span>
<span data-ttu-id="0f503-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f503-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f503-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f503-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f503-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0f503-124">INPUTS</span></span>

### <span data-ttu-id="0f503-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="0f503-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f503-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0f503-126">System.String</span></span>

## <span data-ttu-id="0f503-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0f503-127">OUTPUTS</span></span>

### <span data-ttu-id="0f503-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementLo用</span><span class="sxs-lookup"><span data-stu-id="0f503-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="0f503-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0f503-129">NOTES</span></span>

## <span data-ttu-id="0f503-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f503-130">RELATED LINKS</span></span>

[<span data-ttu-id="0f503-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0f503-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="0f503-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0f503-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="0f503-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0f503-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


