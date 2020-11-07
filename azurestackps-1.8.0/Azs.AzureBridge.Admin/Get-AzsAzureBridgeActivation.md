---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "93802718"
---
# <span data-ttu-id="a2f9e-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="a2f9e-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="a2f9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f9e-103">傳回 Azure 橋接器啟用。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="a2f9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2f9e-104">SYNTAX</span></span>

### <span data-ttu-id="a2f9e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a2f9e-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a2f9e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a2f9e-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="a2f9e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f9e-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a2f9e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2f9e-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f9e-109">在註冊 Azure 堆疊之後，啟用物件就會包含將 Azure 堆疊部署連結至 Azure 中的註冊（例如註冊到期日、名稱等）的資訊。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="a2f9e-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2f9e-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f9e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a2f9e-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="a2f9e-112">取得資源群組「activationRG」下的 Azure 橋接器啟用清單</span><span class="sxs-lookup"><span data-stu-id="a2f9e-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="a2f9e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a2f9e-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="a2f9e-114">透過 [activationRG] 底下的名稱 "myActivation" 取得 Azure 橋接器啟用</span><span class="sxs-lookup"><span data-stu-id="a2f9e-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="a2f9e-115">參數</span><span class="sxs-lookup"><span data-stu-id="a2f9e-115">PARAMETERS</span></span>

### <span data-ttu-id="a2f9e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2f9e-116">-Name</span></span>
<span data-ttu-id="a2f9e-117">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f9e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f9e-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2f9e-119">在註冊 Azure 堆疊期間使用的資源群組;您也可以在入口網站中查看資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f9e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f9e-120">-ResourceId</span></span>
<span data-ttu-id="a2f9e-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f9e-122">-略過</span><span class="sxs-lookup"><span data-stu-id="a2f9e-122">-Skip</span></span>
<span data-ttu-id="a2f9e-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f9e-124">-上方</span><span class="sxs-lookup"><span data-stu-id="a2f9e-124">-Top</span></span>
<span data-ttu-id="a2f9e-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a2f9e-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f9e-127">CommonParameters</span></span>
<span data-ttu-id="a2f9e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f9e-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2f9e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f9e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a2f9e-130">INPUTS</span></span>

## <span data-ttu-id="a2f9e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a2f9e-131">OUTPUTS</span></span>

### <span data-ttu-id="a2f9e-132">AzureStack AzureBridge. ActivationResource （）</span><span class="sxs-lookup"><span data-stu-id="a2f9e-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="a2f9e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a2f9e-133">NOTES</span></span>

## <span data-ttu-id="a2f9e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2f9e-134">RELATED LINKS</span></span>
