---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448503"
---
# <span data-ttu-id="66842-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="66842-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="66842-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66842-102">SYNOPSIS</span></span>
<span data-ttu-id="66842-103">取得 Analysis Services 伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="66842-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66842-104">句法</span><span class="sxs-lookup"><span data-stu-id="66842-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66842-105">說明</span><span class="sxs-lookup"><span data-stu-id="66842-105">DESCRIPTION</span></span>
<span data-ttu-id="66842-106">Get-AzureRmAnalysisServicesServer Cmdlet 會取得 Analysis Services 伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="66842-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="66842-107">示例</span><span class="sxs-lookup"><span data-stu-id="66842-107">EXAMPLES</span></span>

### <span data-ttu-id="66842-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66842-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="66842-109">這個命令會取得名為 ResourceGroup03 的資源群組中的所有 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="66842-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="66842-110">範例2：取得伺服器</span><span class="sxs-lookup"><span data-stu-id="66842-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="66842-111">這個命令會在名為 ResourceGroup03 的資源群組中取得名為 testserver 的 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="66842-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="66842-112">參數</span><span class="sxs-lookup"><span data-stu-id="66842-112">PARAMETERS</span></span>

### <span data-ttu-id="66842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66842-113">-DefaultProfile</span></span>
<span data-ttu-id="66842-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66842-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66842-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="66842-115">-Name</span></span>
<span data-ttu-id="66842-116">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="66842-116">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66842-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66842-117">-ResourceGroupName</span></span>
<span data-ttu-id="66842-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="66842-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66842-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66842-119">CommonParameters</span></span>
<span data-ttu-id="66842-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66842-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66842-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66842-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66842-122">輸入</span><span class="sxs-lookup"><span data-stu-id="66842-122">INPUTS</span></span>

### <span data-ttu-id="66842-123">System.object</span><span class="sxs-lookup"><span data-stu-id="66842-123">System.String</span></span>

## <span data-ttu-id="66842-124">輸出</span><span class="sxs-lookup"><span data-stu-id="66842-124">OUTPUTS</span></span>

### <span data-ttu-id="66842-125">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="66842-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="66842-126">筆記</span><span class="sxs-lookup"><span data-stu-id="66842-126">NOTES</span></span>
<span data-ttu-id="66842-127">別名： Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="66842-127">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="66842-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="66842-128">RELATED LINKS</span></span>

[<span data-ttu-id="66842-129">新-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="66842-129">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="66842-130">移除-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="66842-130">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
