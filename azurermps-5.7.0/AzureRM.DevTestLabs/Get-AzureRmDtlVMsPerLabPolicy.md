---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 83b061c646d8d6f75689d6a67fe163c43456edb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448679"
---
# <span data-ttu-id="f5f6a-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f5f6a-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="f5f6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f6a-103">取得 DevTest 實驗中實驗室的每個實驗室原則的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5f6a-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f6a-106">**AzureRmDtlVMsPerLabPolicy** Cmdlet 會取得實驗室的每個實驗室原則的虛擬機器，這可讓您設定實驗室所允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="f5f6a-107">這個 Cmdlet 會傳回原則的啟用或停用狀態，以及您在原則中設定的實驗中所允許的虛擬機器總數量。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="f5f6a-108">示例</span><span class="sxs-lookup"><span data-stu-id="f5f6a-108">EXAMPLES</span></span>

## <span data-ttu-id="f5f6a-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5f6a-109">PARAMETERS</span></span>

### <span data-ttu-id="f5f6a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f6a-110">-DefaultProfile</span></span>
<span data-ttu-id="f5f6a-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f5f6a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5f6a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="f5f6a-112">-LabName</span></span>
<span data-ttu-id="f5f6a-113">指定此 Cmdlet 取得虛擬機器之實驗的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="f5f6a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f6a-114">-ResourceGroupName</span></span>
<span data-ttu-id="f5f6a-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f6a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f6a-116">CommonParameters</span></span>
<span data-ttu-id="f5f6a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f6a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f6a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f5f6a-119">INPUTS</span></span>

### <span data-ttu-id="f5f6a-120">所有</span><span class="sxs-lookup"><span data-stu-id="f5f6a-120">None</span></span>
<span data-ttu-id="f5f6a-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5f6a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f5f6a-122">OUTPUTS</span></span>

### <span data-ttu-id="f5f6a-123">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="f5f6a-124">這個 Cmdlet 會傳回指定可在 lab 中建立的虛擬機器數上限的原則。</span><span class="sxs-lookup"><span data-stu-id="f5f6a-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="f5f6a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f5f6a-125">NOTES</span></span>

## <span data-ttu-id="f5f6a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5f6a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5f6a-127">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="f5f6a-127">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


