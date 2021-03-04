---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: a4a6cf459c253c26f5d550492f8b756d59fcdf44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912942"
---
# <span data-ttu-id="870f9-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="870f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="870f9-102">SYNOPSIS</span></span>
<span data-ttu-id="870f9-103">獲得清單或特定的 API 管理服務描述。</span><span class="sxs-lookup"><span data-stu-id="870f9-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="870f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="870f9-104">SYNTAX</span></span>

### <span data-ttu-id="870f9-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="870f9-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="870f9-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="870f9-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="870f9-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="870f9-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="870f9-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="870f9-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="870f9-109">描述</span><span class="sxs-lookup"><span data-stu-id="870f9-109">DESCRIPTION</span></span>
<span data-ttu-id="870f9-110">**Get-AzApiManagement** Cmdlet 會取得訂閱或指定資源群組或特定 API 管理下的所有 API 管理服務清單。</span><span class="sxs-lookup"><span data-stu-id="870f9-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="870f9-111">例子</span><span class="sxs-lookup"><span data-stu-id="870f9-111">EXAMPLES</span></span>

### <span data-ttu-id="870f9-112">範例 1：取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="870f9-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="870f9-113">此命令會獲得訂閱內的所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="870f9-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="870f9-114">範例 2：以特定名稱取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="870f9-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="870f9-115">此命令會按名稱獲得所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="870f9-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="870f9-116">參數</span><span class="sxs-lookup"><span data-stu-id="870f9-116">PARAMETERS</span></span>

### <span data-ttu-id="870f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870f9-117">-DefaultProfile</span></span>
<span data-ttu-id="870f9-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="870f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="870f9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="870f9-119">-Name</span></span>
<span data-ttu-id="870f9-120">指定 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="870f9-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="870f9-122">指定此 Cmdlet 在哪個資源組名下會獲得 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="870f9-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870f9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="870f9-123">-ResourceId</span></span>
<span data-ttu-id="870f9-124">API 管理服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="870f9-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870f9-125">CommonParameters</span></span>
<span data-ttu-id="870f9-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="870f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870f9-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="870f9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870f9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="870f9-128">INPUTS</span></span>

### <span data-ttu-id="870f9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="870f9-129">System.String</span></span>

## <span data-ttu-id="870f9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="870f9-130">OUTPUTS</span></span>

### <span data-ttu-id="870f9-131">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="870f9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="870f9-132">NOTES</span></span>

## <span data-ttu-id="870f9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="870f9-133">RELATED LINKS</span></span>

[<span data-ttu-id="870f9-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="870f9-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="870f9-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="870f9-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="870f9-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


