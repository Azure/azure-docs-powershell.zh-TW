---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447444"
---
# <span data-ttu-id="e7de3-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e7de3-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="e7de3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7de3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7de3-103">建立新的閘道實體。</span><span class="sxs-lookup"><span data-stu-id="e7de3-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="e7de3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7de3-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7de3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7de3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7de3-106">**新的-AzApiManagementGateway** Cmdlet 會建立新的閘道實體。</span><span class="sxs-lookup"><span data-stu-id="e7de3-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="e7de3-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7de3-107">EXAMPLES</span></span>

### <span data-ttu-id="e7de3-108">範例1：建立閘道</span><span class="sxs-lookup"><span data-stu-id="e7de3-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="e7de3-109">這個命令會建立閘道。</span><span class="sxs-lookup"><span data-stu-id="e7de3-109">This command creates a gateway.</span></span>

## <span data-ttu-id="e7de3-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7de3-110">PARAMETERS</span></span>

### <span data-ttu-id="e7de3-111">-內容</span><span class="sxs-lookup"><span data-stu-id="e7de3-111">-Context</span></span>
<span data-ttu-id="e7de3-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e7de3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e7de3-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e7de3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e7de3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7de3-114">-DefaultProfile</span></span>
<span data-ttu-id="e7de3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7de3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7de3-116">-描述</span><span class="sxs-lookup"><span data-stu-id="e7de3-116">-Description</span></span>
<span data-ttu-id="e7de3-117">閘道描述。</span><span class="sxs-lookup"><span data-stu-id="e7de3-117">Gateway description.</span></span>
<span data-ttu-id="e7de3-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e7de3-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7de3-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e7de3-119">-GatewayId</span></span>
<span data-ttu-id="e7de3-120">新閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7de3-120">Identifier of new gateway.</span></span>
<span data-ttu-id="e7de3-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e7de3-121">This parameter is optional.</span></span>
<span data-ttu-id="e7de3-122">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="e7de3-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e7de3-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="e7de3-123">-LocationData</span></span>
<span data-ttu-id="e7de3-124">閘道位置。</span><span class="sxs-lookup"><span data-stu-id="e7de3-124">Gateway location.</span></span>
<span data-ttu-id="e7de3-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e7de3-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7de3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e7de3-126">-Confirm</span></span>
<span data-ttu-id="e7de3-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7de3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7de3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7de3-128">-WhatIf</span></span>
<span data-ttu-id="e7de3-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7de3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7de3-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7de3-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7de3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7de3-131">CommonParameters</span></span>
<span data-ttu-id="e7de3-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7de3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7de3-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7de3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7de3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e7de3-134">INPUTS</span></span>

### <span data-ttu-id="e7de3-135">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e7de3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e7de3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e7de3-136">System.String</span></span>

### <span data-ttu-id="e7de3-137">ServiceManagement. PsApiManagementResourceLocation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e7de3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e7de3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e7de3-138">OUTPUTS</span></span>

### <span data-ttu-id="e7de3-139">ServiceManagement. PsApiManagementGateway （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e7de3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="e7de3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e7de3-140">NOTES</span></span>

## <span data-ttu-id="e7de3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7de3-141">RELATED LINKS</span></span>
