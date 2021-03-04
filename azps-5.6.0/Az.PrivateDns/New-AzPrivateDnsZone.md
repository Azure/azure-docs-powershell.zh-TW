---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: d135cc72a9830535d6b67ce80f29725a569894e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908369"
---
# <span data-ttu-id="806d3-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="806d3-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="806d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="806d3-102">SYNOPSIS</span></span>
<span data-ttu-id="806d3-103">建立新的私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="806d3-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="806d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="806d3-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="806d3-105">DESCRIPTION</span></span>
<span data-ttu-id="806d3-106">**New-AzPrivateDnsZone Cmdlet** 會建立一個新的私人網域名稱系統 (DNS) 指定資源群組中的區域。</span><span class="sxs-lookup"><span data-stu-id="806d3-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="806d3-107">您必須為 Name 參數指定唯一的專用DNS 區功能變數名稱稱，否則 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="806d3-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="806d3-108">建立區域之後，請使用 New-AzPrivateDnsRecordSet Cmdlet 在區域中建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="806d3-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="806d3-109">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="806d3-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="806d3-110">例子</span><span class="sxs-lookup"><span data-stu-id="806d3-110">EXAMPLES</span></span>

### <span data-ttu-id="806d3-111">範例 1：建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="806d3-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="806d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="806d3-112">PARAMETERS</span></span>

### <span data-ttu-id="806d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806d3-113">-DefaultProfile</span></span>
<span data-ttu-id="806d3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="806d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="806d3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="806d3-115">-Name</span></span>
<span data-ttu-id="806d3-116">指定要建立的私人 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="806d3-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="806d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="806d3-118">指定要建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="806d3-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="806d3-119">-標記</span><span class="sxs-lookup"><span data-stu-id="806d3-119">-Tag</span></span>
<span data-ttu-id="806d3-120">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="806d3-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="806d3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="806d3-121">-Confirm</span></span>
<span data-ttu-id="806d3-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="806d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="806d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806d3-123">-WhatIf</span></span>
<span data-ttu-id="806d3-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="806d3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="806d3-125">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="806d3-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="806d3-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="806d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="806d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806d3-127">CommonParameters</span></span>
<span data-ttu-id="806d3-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="806d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806d3-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="806d3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806d3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="806d3-130">INPUTS</span></span>

### <span data-ttu-id="806d3-131">沒有</span><span class="sxs-lookup"><span data-stu-id="806d3-131">None</span></span>

## <span data-ttu-id="806d3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="806d3-132">OUTPUTS</span></span>

### <span data-ttu-id="806d3-133">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="806d3-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="806d3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="806d3-134">NOTES</span></span>

## <span data-ttu-id="806d3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="806d3-135">RELATED LINKS</span></span>

[<span data-ttu-id="806d3-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="806d3-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="806d3-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="806d3-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="806d3-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="806d3-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
