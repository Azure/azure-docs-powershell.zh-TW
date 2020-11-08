---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129570"
---
# <span data-ttu-id="418d3-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="418d3-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="418d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="418d3-102">SYNOPSIS</span></span>
<span data-ttu-id="418d3-103">取得 DevTest 實驗中實驗室的每個實驗室原則的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="418d3-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="418d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="418d3-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="418d3-105">說明</span><span class="sxs-lookup"><span data-stu-id="418d3-105">DESCRIPTION</span></span>
<span data-ttu-id="418d3-106">**AzDtlVMsPerLabPolicy** Cmdlet 會取得實驗室的每個實驗室原則的虛擬機器，這可讓您設定實驗室所允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="418d3-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="418d3-107">這個 Cmdlet 會傳回原則的啟用或停用狀態，以及您在原則中設定的實驗中所允許的虛擬機器總數量。</span><span class="sxs-lookup"><span data-stu-id="418d3-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="418d3-108">示例</span><span class="sxs-lookup"><span data-stu-id="418d3-108">EXAMPLES</span></span>

## <span data-ttu-id="418d3-109">參數</span><span class="sxs-lookup"><span data-stu-id="418d3-109">PARAMETERS</span></span>

### <span data-ttu-id="418d3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418d3-110">-DefaultProfile</span></span>
<span data-ttu-id="418d3-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="418d3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="418d3-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="418d3-112">-LabName</span></span>
<span data-ttu-id="418d3-113">指定此 Cmdlet 取得虛擬機器之實驗的名稱。</span><span class="sxs-lookup"><span data-stu-id="418d3-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418d3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418d3-114">-ResourceGroupName</span></span>
<span data-ttu-id="418d3-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="418d3-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418d3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418d3-116">CommonParameters</span></span>
<span data-ttu-id="418d3-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="418d3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418d3-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="418d3-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418d3-119">輸入</span><span class="sxs-lookup"><span data-stu-id="418d3-119">INPUTS</span></span>

### <span data-ttu-id="418d3-120">System.object</span><span class="sxs-lookup"><span data-stu-id="418d3-120">System.String</span></span>

## <span data-ttu-id="418d3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="418d3-121">OUTPUTS</span></span>

### <span data-ttu-id="418d3-122">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="418d3-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="418d3-123">筆記</span><span class="sxs-lookup"><span data-stu-id="418d3-123">NOTES</span></span>

## <span data-ttu-id="418d3-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="418d3-124">RELATED LINKS</span></span>

[<span data-ttu-id="418d3-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="418d3-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


