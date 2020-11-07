---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 2aa0c6516614adb5fae84e2d141cf1882de71628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626642"
---
# <span data-ttu-id="5ba38-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ba38-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="5ba38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ba38-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba38-103">取得主廚延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ba38-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba38-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ba38-104">SYNTAX</span></span>

### <span data-ttu-id="5ba38-105">Linux</span><span class="sxs-lookup"><span data-stu-id="5ba38-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba38-106">時間</span><span class="sxs-lookup"><span data-stu-id="5ba38-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba38-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ba38-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba38-108">**AzureVMChefExtension** Cmdlet 會取得在虛擬機器上安裝的主廚擴充功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ba38-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="5ba38-109">示例</span><span class="sxs-lookup"><span data-stu-id="5ba38-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba38-110">範例1：取得 Windows 虛擬機器主廚延伸的詳細資料-</span><span class="sxs-lookup"><span data-stu-id="5ba38-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="5ba38-111">這個命令會從屬於名為 ResourceGroup001 之資源群組的名為 WindowsVM001 的 Windows 虛擬機器中取得主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="5ba38-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="5ba38-112">範例2：取得 Linux 虛擬機器主廚延伸的詳細資料</span><span class="sxs-lookup"><span data-stu-id="5ba38-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="5ba38-113">這個命令會從屬於名為 ResourceGroup002 之資源群組的 Linux 虛擬機器中取得主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="5ba38-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="5ba38-114">參數</span><span class="sxs-lookup"><span data-stu-id="5ba38-114">PARAMETERS</span></span>

### <span data-ttu-id="5ba38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba38-115">-DefaultProfile</span></span>
<span data-ttu-id="5ba38-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ba38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba38-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="5ba38-117">-Linux</span></span>
<span data-ttu-id="5ba38-118">表示此 Cmdlet 可在 Linux 虛擬機器上運作。</span><span class="sxs-lookup"><span data-stu-id="5ba38-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba38-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ba38-119">-Name</span></span>
<span data-ttu-id="5ba38-120">指定主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ba38-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba38-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ba38-122">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ba38-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="5ba38-123">-狀態</span><span class="sxs-lookup"><span data-stu-id="5ba38-123">-Status</span></span>
<span data-ttu-id="5ba38-124">表示此 Cmdlet 只會取得主廚延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="5ba38-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba38-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="5ba38-125">-VMName</span></span>
<span data-ttu-id="5ba38-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ba38-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba38-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="5ba38-127">-Windows</span></span>
<span data-ttu-id="5ba38-128">表示此 Cmdlet 適用于 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5ba38-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba38-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba38-129">CommonParameters</span></span>
<span data-ttu-id="5ba38-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ba38-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba38-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ba38-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba38-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5ba38-132">INPUTS</span></span>

## <span data-ttu-id="5ba38-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5ba38-133">OUTPUTS</span></span>

## <span data-ttu-id="5ba38-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5ba38-134">NOTES</span></span>

## <span data-ttu-id="5ba38-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ba38-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ba38-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ba38-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="5ba38-137">移除-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5ba38-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


