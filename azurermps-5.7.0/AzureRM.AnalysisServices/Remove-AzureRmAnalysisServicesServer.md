---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 541f1a2039f8c7b54a71798432a9f009d57144c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452296"
---
# <span data-ttu-id="877e3-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="877e3-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="877e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="877e3-102">SYNOPSIS</span></span>
<span data-ttu-id="877e3-103">刪除 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="877e3-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="877e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="877e3-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="877e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="877e3-105">DESCRIPTION</span></span>
<span data-ttu-id="877e3-106">Remove-AzureRmAnalysisServicesServer Cmdlet 會刪除 Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="877e3-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="877e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="877e3-107">EXAMPLES</span></span>

### <span data-ttu-id="877e3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="877e3-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="877e3-109">這個命令會在 resourcegroup testgroup 中移除名為 testserver 的伺服器</span><span class="sxs-lookup"><span data-stu-id="877e3-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="877e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="877e3-110">PARAMETERS</span></span>

### <span data-ttu-id="877e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877e3-111">-DefaultProfile</span></span>
<span data-ttu-id="877e3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="877e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="877e3-113">-Name</span></span>
<span data-ttu-id="877e3-114">Analysis Services 伺服器的名稱</span><span class="sxs-lookup"><span data-stu-id="877e3-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="877e3-115">-PassThru</span></span>
<span data-ttu-id="877e3-116">如果作業成功完成，將會傳回已刪除伺服器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="877e3-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="877e3-118">伺服器所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="877e3-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="877e3-119">-Confirm</span></span>
<span data-ttu-id="877e3-120">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="877e3-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="877e3-121">-WhatIf</span></span>
<span data-ttu-id="877e3-122">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="877e3-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877e3-123">CommonParameters</span></span>
<span data-ttu-id="877e3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="877e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877e3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="877e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877e3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="877e3-126">INPUTS</span></span>

### <span data-ttu-id="877e3-127">所有</span><span class="sxs-lookup"><span data-stu-id="877e3-127">None</span></span>
<span data-ttu-id="877e3-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="877e3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="877e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="877e3-129">OUTPUTS</span></span>

### <span data-ttu-id="877e3-130">AzureAnalysisServicesServer 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="877e3-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="877e3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="877e3-131">NOTES</span></span>
<span data-ttu-id="877e3-132">別名： Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="877e3-132">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="877e3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="877e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="877e3-134">AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="877e3-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="877e3-135">新-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="877e3-135">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
