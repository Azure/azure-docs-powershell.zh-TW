---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "93968769"
---
# <span data-ttu-id="e7f65-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="e7f65-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="e7f65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7f65-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f65-103">傳回 Azure 橋接器啟用。</span><span class="sxs-lookup"><span data-stu-id="e7f65-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="e7f65-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7f65-104">SYNTAX</span></span>

### <span data-ttu-id="e7f65-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e7f65-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e7f65-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e7f65-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="e7f65-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f65-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e7f65-108">說明</span><span class="sxs-lookup"><span data-stu-id="e7f65-108">DESCRIPTION</span></span>
<span data-ttu-id="e7f65-109">在註冊 Azure 堆疊之後，啟用物件就會包含將 Azure 堆疊部署連結至 Azure 中的註冊（例如註冊到期日、名稱等）的資訊。</span><span class="sxs-lookup"><span data-stu-id="e7f65-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="e7f65-110">示例</span><span class="sxs-lookup"><span data-stu-id="e7f65-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f65-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e7f65-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e7f65-112">取得資源群組「activationRG」下的 Azure 橋接器啟用清單</span><span class="sxs-lookup"><span data-stu-id="e7f65-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="e7f65-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e7f65-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e7f65-114">透過 [activationRG] 底下的名稱 "myActivation" 取得 Azure 橋接器啟用</span><span class="sxs-lookup"><span data-stu-id="e7f65-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="e7f65-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7f65-115">PARAMETERS</span></span>

### <span data-ttu-id="e7f65-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7f65-116">-Name</span></span>
<span data-ttu-id="e7f65-117">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7f65-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f65-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f65-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7f65-119">在註冊 Azure 堆疊期間使用的資源群組;您也可以在入口網站中查看資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7f65-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f65-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f65-120">-ResourceId</span></span>
<span data-ttu-id="e7f65-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e7f65-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f65-122">-略過</span><span class="sxs-lookup"><span data-stu-id="e7f65-122">-Skip</span></span>
<span data-ttu-id="e7f65-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e7f65-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e7f65-124">-上方</span><span class="sxs-lookup"><span data-stu-id="e7f65-124">-Top</span></span>
<span data-ttu-id="e7f65-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e7f65-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e7f65-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="e7f65-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e7f65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f65-127">CommonParameters</span></span>
<span data-ttu-id="e7f65-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7f65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f65-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7f65-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f65-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e7f65-130">INPUTS</span></span>

## <span data-ttu-id="e7f65-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e7f65-131">OUTPUTS</span></span>

### <span data-ttu-id="e7f65-132">AzureStack AzureBridge. ActivationResource （）</span><span class="sxs-lookup"><span data-stu-id="e7f65-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="e7f65-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e7f65-133">NOTES</span></span>

## <span data-ttu-id="e7f65-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7f65-134">RELATED LINKS</span></span>

