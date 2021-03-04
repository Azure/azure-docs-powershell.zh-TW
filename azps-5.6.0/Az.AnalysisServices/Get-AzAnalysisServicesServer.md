---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: 8c2e7b9fe5335df29308a612ef8a133762e7ab4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917806"
---
# <span data-ttu-id="95333-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="95333-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="95333-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95333-102">SYNOPSIS</span></span>
<span data-ttu-id="95333-103">獲得 Analysis Services 伺服器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="95333-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="95333-104">語法</span><span class="sxs-lookup"><span data-stu-id="95333-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95333-105">描述</span><span class="sxs-lookup"><span data-stu-id="95333-105">DESCRIPTION</span></span>
<span data-ttu-id="95333-106">此Get-AzAnalysisServicesServer Cmdlet 會獲得 Analysis Services 伺服器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="95333-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="95333-107">例子</span><span class="sxs-lookup"><span data-stu-id="95333-107">EXAMPLES</span></span>

### <span data-ttu-id="95333-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="95333-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="95333-109">此命令會獲得資源群組中名為 ResourceGroup03 的所有 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="95333-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="95333-110">範例 2：取得伺服器</span><span class="sxs-lookup"><span data-stu-id="95333-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="95333-111">此命令會獲得名為 ResourceGroup03 的資源群組中名為 testserver 的 Azure Analysis Services 伺服器。</span><span class="sxs-lookup"><span data-stu-id="95333-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="95333-112">參數</span><span class="sxs-lookup"><span data-stu-id="95333-112">PARAMETERS</span></span>

### <span data-ttu-id="95333-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95333-113">-DefaultProfile</span></span>
<span data-ttu-id="95333-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="95333-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95333-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="95333-115">-Name</span></span>
<span data-ttu-id="95333-116">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="95333-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="95333-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95333-117">-ResourceGroupName</span></span>
<span data-ttu-id="95333-118">伺服器所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="95333-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="95333-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95333-119">CommonParameters</span></span>
<span data-ttu-id="95333-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95333-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95333-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="95333-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95333-122">輸入</span><span class="sxs-lookup"><span data-stu-id="95333-122">INPUTS</span></span>

### <span data-ttu-id="95333-123">System.String</span><span class="sxs-lookup"><span data-stu-id="95333-123">System.String</span></span>

## <span data-ttu-id="95333-124">輸出</span><span class="sxs-lookup"><span data-stu-id="95333-124">OUTPUTS</span></span>

### <span data-ttu-id="95333-125">Microsoft.Azure.Commands.AnalysisServices.models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="95333-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="95333-126">筆記</span><span class="sxs-lookup"><span data-stu-id="95333-126">NOTES</span></span>
<span data-ttu-id="95333-127">別名：Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="95333-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="95333-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="95333-128">RELATED LINKS</span></span>

[<span data-ttu-id="95333-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="95333-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="95333-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="95333-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
