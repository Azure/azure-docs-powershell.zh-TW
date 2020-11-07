---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624203"
---
# <span data-ttu-id="35589-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="35589-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="35589-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35589-102">SYNOPSIS</span></span>
<span data-ttu-id="35589-103">取得 .rdp 檔案。</span><span class="sxs-lookup"><span data-stu-id="35589-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35589-104">句法</span><span class="sxs-lookup"><span data-stu-id="35589-104">SYNTAX</span></span>

### <span data-ttu-id="35589-105">內容</span><span class="sxs-lookup"><span data-stu-id="35589-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="35589-106">發起</span><span class="sxs-lookup"><span data-stu-id="35589-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="35589-107">說明</span><span class="sxs-lookup"><span data-stu-id="35589-107">DESCRIPTION</span></span>
<span data-ttu-id="35589-108">**AzureRmRemoteDesktopFile** Cmdlet 會取得遠端桌面通訊協定 ( .rdp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="35589-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="35589-109">示例</span><span class="sxs-lookup"><span data-stu-id="35589-109">EXAMPLES</span></span>

### <span data-ttu-id="35589-110">範例1：取得遠端桌面檔案</span><span class="sxs-lookup"><span data-stu-id="35589-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="35589-111">這個命令會取得名為 VirtualMachine07 的虛擬機器的遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="35589-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="35589-112">該命令會將結果儲存在名為 D:\RemoteDesktopFile07.rdp. 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="35589-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="35589-113">參數</span><span class="sxs-lookup"><span data-stu-id="35589-113">PARAMETERS</span></span>

### <span data-ttu-id="35589-114">-啟動</span><span class="sxs-lookup"><span data-stu-id="35589-114">-Launch</span></span>
<span data-ttu-id="35589-115">表示此 Cmdlet 會在取得 .rdp 檔案後啟動遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="35589-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35589-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="35589-116">-LocalPath</span></span>
<span data-ttu-id="35589-117">指定此 Cmdlet 儲存 .rdp 檔案的本機完整路徑。</span><span class="sxs-lookup"><span data-stu-id="35589-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35589-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="35589-118">-Name</span></span>
<span data-ttu-id="35589-119">指定此 Cmdlet 所取得之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="35589-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35589-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35589-120">-ResourceGroupName</span></span>
<span data-ttu-id="35589-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35589-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="35589-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35589-122">CommonParameters</span></span>
<span data-ttu-id="35589-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35589-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35589-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35589-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35589-125">輸入</span><span class="sxs-lookup"><span data-stu-id="35589-125">INPUTS</span></span>

### <span data-ttu-id="35589-126">所有</span><span class="sxs-lookup"><span data-stu-id="35589-126">None</span></span>
<span data-ttu-id="35589-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="35589-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35589-128">輸出</span><span class="sxs-lookup"><span data-stu-id="35589-128">OUTPUTS</span></span>

## <span data-ttu-id="35589-129">筆記</span><span class="sxs-lookup"><span data-stu-id="35589-129">NOTES</span></span>

## <span data-ttu-id="35589-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="35589-130">RELATED LINKS</span></span>

