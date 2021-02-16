---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141735"
---
# <span data-ttu-id="2b3cc-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="2b3cc-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="2b3cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3cc-103">取得現有閘道的金鑰</span><span class="sxs-lookup"><span data-stu-id="2b3cc-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="2b3cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b3cc-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b3cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3cc-106">**AzApiManagementGatewayKey** Cmdlet 會取得現有閘道的金鑰</span><span class="sxs-lookup"><span data-stu-id="2b3cc-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="2b3cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="2b3cc-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3cc-108">範例2：依識別碼取得閘道</span><span class="sxs-lookup"><span data-stu-id="2b3cc-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="2b3cc-109">這個命令會取得「0123456789」閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="2b3cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b3cc-110">PARAMETERS</span></span>

### <span data-ttu-id="2b3cc-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2b3cc-111">-Context</span></span>
<span data-ttu-id="2b3cc-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b3cc-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2b3cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3cc-114">-DefaultProfile</span></span>
<span data-ttu-id="2b3cc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b3cc-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2b3cc-116">-GatewayId</span></span>
<span data-ttu-id="2b3cc-117">閘道識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-117">Gateway identifier.</span></span>
<span data-ttu-id="2b3cc-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2b3cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3cc-119">CommonParameters</span></span>
<span data-ttu-id="2b3cc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3cc-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b3cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3cc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2b3cc-122">INPUTS</span></span>

### <span data-ttu-id="2b3cc-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2b3cc-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b3cc-124">System.object</span><span class="sxs-lookup"><span data-stu-id="2b3cc-124">System.String</span></span>

## <span data-ttu-id="2b3cc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2b3cc-125">OUTPUTS</span></span>

### <span data-ttu-id="2b3cc-126">ServiceManagement. PsApiManagementGatewayKey （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2b3cc-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="2b3cc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2b3cc-127">NOTES</span></span>

## <span data-ttu-id="2b3cc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b3cc-128">RELATED LINKS</span></span>
