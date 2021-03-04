---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: 08931af2c5d4f4747bd02a759e374d8fccd247c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909253"
---
# <span data-ttu-id="47c33-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="47c33-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="47c33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47c33-102">SYNOPSIS</span></span>
<span data-ttu-id="47c33-103">獲得現有閘道的金鑰</span><span class="sxs-lookup"><span data-stu-id="47c33-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="47c33-104">語法</span><span class="sxs-lookup"><span data-stu-id="47c33-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47c33-105">描述</span><span class="sxs-lookup"><span data-stu-id="47c33-105">DESCRIPTION</span></span>
<span data-ttu-id="47c33-106">**Get-AzApiManagementGatewayKey** Cmdlet 會取得現有閘道的金鑰</span><span class="sxs-lookup"><span data-stu-id="47c33-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="47c33-107">例子</span><span class="sxs-lookup"><span data-stu-id="47c33-107">EXAMPLES</span></span>

### <span data-ttu-id="47c33-108">範例 2：以識別碼取得閘道</span><span class="sxs-lookup"><span data-stu-id="47c33-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="47c33-109">此命令會獲得「0123456789」閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="47c33-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="47c33-110">參數</span><span class="sxs-lookup"><span data-stu-id="47c33-110">PARAMETERS</span></span>

### <span data-ttu-id="47c33-111">-內容</span><span class="sxs-lookup"><span data-stu-id="47c33-111">-Context</span></span>
<span data-ttu-id="47c33-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="47c33-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47c33-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47c33-113">This parameter is required.</span></span>

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

### <span data-ttu-id="47c33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c33-114">-DefaultProfile</span></span>
<span data-ttu-id="47c33-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47c33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c33-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="47c33-116">-GatewayId</span></span>
<span data-ttu-id="47c33-117">閘道識別碼。</span><span class="sxs-lookup"><span data-stu-id="47c33-117">Gateway identifier.</span></span>
<span data-ttu-id="47c33-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47c33-118">This parameter is required.</span></span>

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

### <span data-ttu-id="47c33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c33-119">CommonParameters</span></span>
<span data-ttu-id="47c33-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47c33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c33-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47c33-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c33-122">輸入</span><span class="sxs-lookup"><span data-stu-id="47c33-122">INPUTS</span></span>

### <span data-ttu-id="47c33-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="47c33-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47c33-124">System.String</span><span class="sxs-lookup"><span data-stu-id="47c33-124">System.String</span></span>

## <span data-ttu-id="47c33-125">輸出</span><span class="sxs-lookup"><span data-stu-id="47c33-125">OUTPUTS</span></span>

### <span data-ttu-id="47c33-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="47c33-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="47c33-127">筆記</span><span class="sxs-lookup"><span data-stu-id="47c33-127">NOTES</span></span>

## <span data-ttu-id="47c33-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="47c33-128">RELATED LINKS</span></span>
