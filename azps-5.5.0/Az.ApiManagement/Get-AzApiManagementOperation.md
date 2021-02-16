---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141711"
---
# <span data-ttu-id="85b20-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="85b20-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="85b20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85b20-102">SYNOPSIS</span></span>
<span data-ttu-id="85b20-103">取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="85b20-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="85b20-104">句法</span><span class="sxs-lookup"><span data-stu-id="85b20-104">SYNTAX</span></span>

### <span data-ttu-id="85b20-105">GetAllApiOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="85b20-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b20-106">GetById</span><span class="sxs-lookup"><span data-stu-id="85b20-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b20-107">說明</span><span class="sxs-lookup"><span data-stu-id="85b20-107">DESCRIPTION</span></span>
<span data-ttu-id="85b20-108">**AzApiManagementOperation** 會取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="85b20-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="85b20-109">示例</span><span class="sxs-lookup"><span data-stu-id="85b20-109">EXAMPLES</span></span>

### <span data-ttu-id="85b20-110">範例1：取得所有 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="85b20-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="85b20-111">這個命令會取得所有 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="85b20-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="85b20-112">範例2：依作業 ID 取得 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="85b20-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="85b20-113">這個命令會透過名為 Operation0003 的操作 ID 取得 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="85b20-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="85b20-114">參數</span><span class="sxs-lookup"><span data-stu-id="85b20-114">PARAMETERS</span></span>

### <span data-ttu-id="85b20-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="85b20-115">-ApiId</span></span>
<span data-ttu-id="85b20-116">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="85b20-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b20-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="85b20-117">-ApiRevision</span></span>
<span data-ttu-id="85b20-118">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="85b20-118">Identifier of API Revision.</span></span> <span data-ttu-id="85b20-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="85b20-119">This parameter is optional.</span></span> <span data-ttu-id="85b20-120">如果未指定，將會從目前使用中的 api 修訂中檢索該作業。</span><span class="sxs-lookup"><span data-stu-id="85b20-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b20-121">-內容</span><span class="sxs-lookup"><span data-stu-id="85b20-121">-Context</span></span>
<span data-ttu-id="85b20-122">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="85b20-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85b20-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b20-123">-DefaultProfile</span></span>
<span data-ttu-id="85b20-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85b20-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b20-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="85b20-125">-OperationId</span></span>
<span data-ttu-id="85b20-126">指定操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="85b20-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b20-127">CommonParameters</span></span>
<span data-ttu-id="85b20-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85b20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b20-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85b20-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b20-130">輸入</span><span class="sxs-lookup"><span data-stu-id="85b20-130">INPUTS</span></span>

### <span data-ttu-id="85b20-131">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="85b20-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="85b20-132">System.object</span><span class="sxs-lookup"><span data-stu-id="85b20-132">System.String</span></span>

## <span data-ttu-id="85b20-133">輸出</span><span class="sxs-lookup"><span data-stu-id="85b20-133">OUTPUTS</span></span>

### <span data-ttu-id="85b20-134">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="85b20-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="85b20-135">筆記</span><span class="sxs-lookup"><span data-stu-id="85b20-135">NOTES</span></span>

## <span data-ttu-id="85b20-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="85b20-136">RELATED LINKS</span></span>

[<span data-ttu-id="85b20-137">新-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="85b20-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="85b20-138">移除-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="85b20-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="85b20-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="85b20-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


