---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 20922936f754f18d2ee26631dc616d9723cdc5e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791965"
---
# <span data-ttu-id="50779-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="50779-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="50779-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50779-102">SYNOPSIS</span></span>
<span data-ttu-id="50779-103">建立新的專用 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="50779-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="50779-104">句法</span><span class="sxs-lookup"><span data-stu-id="50779-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50779-105">說明</span><span class="sxs-lookup"><span data-stu-id="50779-105">DESCRIPTION</span></span>
<span data-ttu-id="50779-106">**新的-AzPrivateDnsZone** Cmdlet 會在指定的資源群組中， (DNS) 區域中建立新的私人網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="50779-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="50779-107">您必須為 *name* 參數指定唯一的專用 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="50779-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="50779-108">建立區域之後，請使用 New-AzPrivateDnsRecordSet Cmdlet 來建立區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="50779-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="50779-109">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50779-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="50779-110">示例</span><span class="sxs-lookup"><span data-stu-id="50779-110">EXAMPLES</span></span>

### <span data-ttu-id="50779-111">範例1：建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="50779-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="50779-112">參數</span><span class="sxs-lookup"><span data-stu-id="50779-112">PARAMETERS</span></span>

### <span data-ttu-id="50779-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50779-113">-DefaultProfile</span></span>
<span data-ttu-id="50779-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="50779-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50779-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="50779-115">-Name</span></span>
<span data-ttu-id="50779-116">指定要建立的專用 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="50779-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50779-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50779-117">-ResourceGroupName</span></span>
<span data-ttu-id="50779-118">指定要在其中建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="50779-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50779-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="50779-119">-Tag</span></span>
<span data-ttu-id="50779-120">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="50779-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50779-121">-確認</span><span class="sxs-lookup"><span data-stu-id="50779-121">-Confirm</span></span>
<span data-ttu-id="50779-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50779-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50779-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50779-123">-WhatIf</span></span>
<span data-ttu-id="50779-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50779-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50779-125">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50779-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50779-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50779-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50779-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50779-127">CommonParameters</span></span>
<span data-ttu-id="50779-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50779-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50779-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50779-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50779-130">輸入</span><span class="sxs-lookup"><span data-stu-id="50779-130">INPUTS</span></span>

### <span data-ttu-id="50779-131">所有</span><span class="sxs-lookup"><span data-stu-id="50779-131">None</span></span>

## <span data-ttu-id="50779-132">輸出</span><span class="sxs-lookup"><span data-stu-id="50779-132">OUTPUTS</span></span>

### <span data-ttu-id="50779-133">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="50779-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="50779-134">筆記</span><span class="sxs-lookup"><span data-stu-id="50779-134">NOTES</span></span>

## <span data-ttu-id="50779-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="50779-135">RELATED LINKS</span></span>

[<span data-ttu-id="50779-136">AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="50779-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="50779-137">新-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="50779-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="50779-138">移除-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="50779-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)