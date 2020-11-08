---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128619"
---
# <span data-ttu-id="9b89b-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9b89b-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="9b89b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b89b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b89b-103">取得 Analysis Services 伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9b89b-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="9b89b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b89b-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b89b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b89b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b89b-106">Get-AzAnalysisServicesServer Cmdlet 會取得 Analysis Services 伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9b89b-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="9b89b-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b89b-107">EXAMPLES</span></span>

### <span data-ttu-id="9b89b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9b89b-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="9b89b-109">這個命令會取得名為 ResourceGroup03 的資源群組中的所有 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9b89b-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="9b89b-110">範例2：取得伺服器</span><span class="sxs-lookup"><span data-stu-id="9b89b-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="9b89b-111">這個命令會在名為 ResourceGroup03 的資源群組中取得名為 testserver 的 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9b89b-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="9b89b-112">參數</span><span class="sxs-lookup"><span data-stu-id="9b89b-112">PARAMETERS</span></span>

### <span data-ttu-id="9b89b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b89b-113">-DefaultProfile</span></span>
<span data-ttu-id="9b89b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b89b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b89b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b89b-115">-Name</span></span>
<span data-ttu-id="9b89b-116">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="9b89b-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9b89b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b89b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b89b-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9b89b-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9b89b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b89b-119">CommonParameters</span></span>
<span data-ttu-id="9b89b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b89b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b89b-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b89b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b89b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9b89b-122">INPUTS</span></span>

### <span data-ttu-id="9b89b-123">System.object</span><span class="sxs-lookup"><span data-stu-id="9b89b-123">System.String</span></span>

## <span data-ttu-id="9b89b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9b89b-124">OUTPUTS</span></span>

### <span data-ttu-id="9b89b-125">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="9b89b-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9b89b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9b89b-126">NOTES</span></span>
<span data-ttu-id="9b89b-127">別名： Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="9b89b-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="9b89b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b89b-128">RELATED LINKS</span></span>

[<span data-ttu-id="9b89b-129">新-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="9b89b-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="9b89b-130">移除-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="9b89b-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)